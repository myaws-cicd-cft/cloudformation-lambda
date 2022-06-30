pipeline {
    agent any 
    stages {
        stage('Submit Stack') {    
            steps {
              sh "aws cloudformation validate-template --template-body file://cftemplate.json --region 'us-east-1'"
              }
          }
     }
}
