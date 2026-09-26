pipeline {
    agent any
    parameters { 
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'Target') 
    }
    stages {
        stage('build') {
            steps { 
                sh 'echo Building' 
            }
        }
        stage('Tests') {
            parallel {
                stage('unit') {
                    steps { 
                        sh 'echo unit tests' 
                    }
                }
                stage('Integration') {
                    steps { 
                        sh 'echo integration tests' 
                    }
                }
            }
        }
         stage('Approve'){
             steps{
             input message: 'Deploy to production'
             }
         }
        stage('Deploy'){
            steps{
                sh 'echo deploying is done'
            }
        }
    } 
} 
    
