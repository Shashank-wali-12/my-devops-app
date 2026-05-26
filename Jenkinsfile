pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/Shashank-wali-12/my-devops-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f my-devops-container || true'
                sh 'docker run -d -p 8090:80 --name my-devops-container my-devops-app'
            }
        }
    }
}
