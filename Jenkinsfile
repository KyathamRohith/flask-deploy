pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'rohith1305/flask-app:latest'
        DOCKER_CREDENTIALS_ID = '7c910bc4-e2e4-48a4-857c-51be93277e96'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/KyathamRohith/flask-deploy', branch: 'main'
            }
        }

        stage('Build and Package') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

       
    post {
        success {
            echo 'Deployment Successful!'
        }
    }
}
}
