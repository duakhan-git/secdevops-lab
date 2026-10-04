pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Security Scan') {
            steps {
                sh 'snyk test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'npm start &'
            }
        }
    }
}
