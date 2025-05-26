@Library('my-shared-lib') _

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh './venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    pythonBuild()  // Calls shared library function
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline complete."
        }
        success {
            echo "✅ Build and tests succeeded."
        }
        failure {
            echo "❌ Build or tests failed."
        }
    }
}
