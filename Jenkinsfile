pipeline {
    agent any
    stages {
        stage('Submit VPC Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name VPC --template-body file://Vpc.yml --parameters file://parameters.json --region 'ap-northeast-1'"
              }
             }
            }
            }
