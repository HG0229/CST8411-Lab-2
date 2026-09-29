/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                bat '''echo Checking out Repository Source Code...'''
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
               bat '''echo Building application...'''
            }
        }
        stage('Test') {
            steps {
                bat '''echo Testing application...'''
                bat 'npm test'
            }
        }
        stage('Deploy') {
            steps {
               bat '''echo Deploying application...'''
            }
        }
    }
}
