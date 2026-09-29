/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                echo 'Checking out Repository Source Code...'
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
            }
        }
    }
}
