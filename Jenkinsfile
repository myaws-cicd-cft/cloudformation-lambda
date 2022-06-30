pipeline {
    agent any 
    stages {
        stage('Validate') {    
            steps {
              sh "aws cloudformation validate-template --template-body file://cftemplate.json --region 'us-east-1'"
              }
          }
        stage('Submit Stack') {    
            steps {
              sh "aws cloudformation update-stack --stack-name HelloWorldJenkins --template-body file://simplests3cft.json --region 'us-east-1'"
              }
          }
     }
}
