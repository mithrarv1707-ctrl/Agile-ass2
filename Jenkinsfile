pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source files...'
            }
        }
        stage('Show Build Info') {
            steps {
                echo "========================================"
                echo "BUILD NUMBER : ${env.BUILD_NUMBER}"
                echo "JOB NAME     : ${env.JOB_NAME}"
                echo "WORKSPACE    : ${env.WORKSPACE}"
                echo "========================================"
            }
        }
        stage('Run Linter') {
            steps {
                echo 'Running flake8 static code analysis...'
                bat 'python -m pip install --quiet flake8'
                bat 'python -m flake8 app.py'
            }
        }
    }
}
