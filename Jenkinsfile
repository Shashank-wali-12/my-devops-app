pipeline {
    agent any

    environment {
        IMAGE_NAME = "shashiwali/myapp:v1"
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Shashank-wali-12/my-devops-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %IMAGE_NAME% .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push %IMAGE_NAME%'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f deployment.yaml'
            }
        }

        stage('Verify Kubernetes') {
            steps {
                bat 'kubectl get pods'
            }
        }
    }
}
