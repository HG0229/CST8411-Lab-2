/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    options {
        skipStageAfterUnstable()
    }
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
                bat './gradlew build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application...'
                bat './gradlew check'
            }
        }
        stage('Deploy') {
            steps {
               echo 'Deploying application...'
            }
        }
    }
}
