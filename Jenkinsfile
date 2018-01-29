#!/usr/bin/env groovy

pipeline {
    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
    post {
        always { 
            echo 'Finished'
        }
        success {
            echo 'Success'
        }
        failure {
            echo 'Failure'
        }
    }
}
