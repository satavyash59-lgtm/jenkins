pipeline {
   agent any
   environment {
        PP_NMAE = 'demo'

   }
   stages {
      stage('Build'){
         environment {
              BUILD_MODE = 'production'
         }
         steps {
             sh 'echo $APP_NAME $BUILD_MODE'
         }
      }
   }
}
