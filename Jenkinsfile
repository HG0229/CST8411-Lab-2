/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.16-eclipse-temurin-21-alpine' } }
    stages {
        stage('Checkout SCM') {
            steps {
                echo 'Checking out Repository Source Code...'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                timeout(time: 3, unit: 'MINUTES') {
                    retry(5) {
                        sh './flakey-deploy.sh'
                    }
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline successful!'
        }
        failure {
            echo 'Pipeline failed. Inspect logs for errors.'
        }
    }
}
