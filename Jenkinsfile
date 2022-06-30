pipeline {
    agent any 
    stages {
        stage('Submit Stack') {
            steps {
              sh "aws cloudformation deploy --template-body file://cftemplate.json --stack-name HelloWorldJenkins --region 'us-east-1' --capabilities CAPABILITY_NAMED_IAM"
            }
        }
    }
}
