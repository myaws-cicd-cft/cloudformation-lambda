pipeline {
    agent any 
    stages {
        stage('Submit Stack') {
            steps {
              sh "aws cloudformation deploy --stack-name HelloWorldJenkins --template-body file://cftemplate.json --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
            }
        }
    }
}
