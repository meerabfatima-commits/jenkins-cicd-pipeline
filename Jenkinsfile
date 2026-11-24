pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code pulled from GitHub'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 --version'
                sh 'python3 -m py_compile app.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest -v'
            }
        }
    }

    post {
        success { echo 'Pipeline succeeded' }
        failure { echo 'Pipeline failed' }
    }
}
