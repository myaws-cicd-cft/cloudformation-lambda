pipeline {
    agent any 
    stages {
        stage('Validate') {    
            steps {
              sh "aws cloudformation validate-template --template-body file://cftemplate.json --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
              }
          }
        stage('Submit Stack') {    
            steps {
              sh "ws cloudformation update-stack --stack-name HelloWorldJenkins --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
              }
          }
     }
}
