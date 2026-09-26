pipeline {
    agent any 
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'target')
    }
    stages {
        stage('Tests') {
            parallel {
                stage('unit') { 
                    steps { sh 'echo unit tests' }
                }
                stage('Integration') { 
                    steps { sh 'echo integration tests' }
                }
            }
           stage('Approve'){
               steps{
                   input message: 'Deploy to production'
               }
           } 
        }
    }

