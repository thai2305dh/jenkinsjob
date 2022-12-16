pipeline {
    agent any
    parameters {
        choice(name: 'environment', choices: ['test', 'dev', 'QA'], description: 'Workspace/environment file to use for deployment')
    }
    stages {
        stage('Submit VPC Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name VPC --template-body file://Vpc.yml --parameters file://${params.envitonment}-parameters.json --region 'ap-northeast-1'"
              }
             }
            }
            }
