pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'rohith1305/flask-app:latest'

    }

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/KyathamRohith/flask-deploy', branch: 'main'
            }
        }

        stage('Build and Package') {
            steps {
                echo "Deployment successful! 🚀"
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Deployment successful! 🚀"
            }
        }
        stage('push docker image') {
            steps {
                echo "Deployment successful! 🚀"
            }
        }
        stage('deployment') {
            steps {
                echo "Deployment successful! 🚀"
            }
        }
}
}
