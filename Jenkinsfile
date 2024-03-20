pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-web-app:latest', '.')
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('my-web-app:latest').run('-p 3000:80 --name my-web-app-container -d')
                }
            }
        }
    }
}
