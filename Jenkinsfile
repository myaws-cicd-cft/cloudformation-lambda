pipeline {
    agent any 
    stages {
        stage('Submit Stack') {
            steps{
               sh "aws validate-template --template-body file://cftemplate.json"
            }
            steps {
              sh "aws cloudformation update-stack --stack-name HelloWorldJenkins --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
            }
        }
    }
}
