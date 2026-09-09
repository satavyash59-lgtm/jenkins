pipeline {
    agent any

    environment {
        APP_NAME = 'demo'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building'
            }
        }

        stage('Test') {
            steps {
                sh 'echo running tests'
            }
        }
    }

    post {
        success {
            echo 'All stages passed'
        }
        failure {
            echo 'Something failed'
        }
    }
}
