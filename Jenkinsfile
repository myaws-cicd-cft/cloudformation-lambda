pipeline {
    agent any 
    stages {
        stage('Validation') {
            steps{
               sh "aws cloudformation validate-template --template-body file://cftemplate.json"
                }
        stage('Submit Stack') {    
            steps {
              sh "aws cloudformation update-stack --stack-name HelloWorldJenkins --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
                }
            }
        }
    }
}
