pipeline {
    agent any

    environment {
        DOCKERHUB_USER = 'samyampradhan'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test Jenkins') {
            steps {
                sh 'echo "Jenkins is working ✔"'
            }
        }

        stage('Test Docker') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Build Frontend Image') {
            steps {
                sh '''
                docker build -t $DOCKERHUB_USER/frontend-test:latest .
                '''
            }
        }
    }
}