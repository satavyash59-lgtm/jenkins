pipeline {
    agent any 
    parameters {
       choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'target')
    }
    stages {
        stage('Deploy') {
            steps {
                sh "echo Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
