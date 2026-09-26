pipeline {
    agent any 
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'target')
    }
    stages {
           stage('Approve'){
               steps{
                   input message: 'Deploy to production'
               }
           } 
        }
    }

