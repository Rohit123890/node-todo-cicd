pipeline{
    agent any
    
    stages{
        stage("Code"){
            steps {
                echo "Cloning the code."
                git url:"https://github.com/Rohit123890/django-notes-app.git", branch:"main"
            }
        }
        stage("Build"){
            steps {
                echo "Building the code."
                sh "docker build . -t my-note-app"
            }
        }
        stage("Test"){
            steps {
                echo "Pushing to dockerhub."
                withCredentials([usernamePassword(credentialsId:"DockerHub",passwordVariable:"DockerHubPass",usernameVariable:"DockerHubUser")]){
                sh "docker tag my-note-app ${env.DockerHubUser}/my-note-app:latest"
                sh "docker login -u ${env.DockerHubUser} -p ${env.DockerHubPass}"
                sh "docker push ${env.DockerHubUser}/my-note-app:latest"
                }
            }
        }
        stage("Deploy"){
            steps {
                echo "Deploying the container"
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
