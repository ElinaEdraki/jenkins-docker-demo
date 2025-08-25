pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ٍElinaEdraki/jenkins-docker-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("jenkins-demo-app")
                }
            }
        }

        stage('Run App in Docker') {
            steps {
                script {
                    docker.image("jenkins-demo-app").run()
                }
            }
        }
    }
}
