pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test Jenkins') {
            steps {
                sh 'echo "Jenkins is working"'
                sh 'ls -la'
            }
        }
    }
}