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
        
