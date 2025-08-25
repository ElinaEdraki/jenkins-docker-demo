pipeline {
    agent any
    
    stages {
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
