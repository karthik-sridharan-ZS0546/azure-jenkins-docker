pipeline {

    agent any

    stages {

        stage('GitHub Checkout') {
            steps {
                echo 'Downloading source code from GitHub'
                checkout scm
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker Image'

                sh 'docker build -t azure-jenkins-demo:1.0 .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                echo 'Checking Docker Image'

                sh 'docker images'
            }
        }

        stage('Success') {
            steps {
                echo 'Jenkins Pipeline Completed Successfully!'
            }
        }
    }
}
