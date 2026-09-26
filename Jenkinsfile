pipeline {
    agent any 
    parameters {
       choice(name: 'ENVIRONMENT', choices: ['staging', 'production','Test'], description: 'target')
    }
    stages {
        stage('Test'){
            parralel {
                stage(unit) { steps { sh 'echo unit tests'}}
                stage('Integration') {steps {sh 'echo integration tests'}}
            }
        }
        }
    }
}
