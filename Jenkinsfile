pipeline {
    agent any
    parameters {
        choice(name: 'environment', choices: ['test', 'dev', 'QA'], description: 'Workspace/environment file to use for deployment')
        choice(name: 'accountid', choices: ['541253215789', '541253215789', '541253215789'], description: 'choose account id for assume role')
    }
    stages {
        stage('Submit VPC Stack') {
            steps {
            withAWS(credentials: 'aws', roleAccount: "${params.accountid}", role:'cross-account-role') {
            sh "aws cloudformation create-stack --stack-name VPC --template-body file://Vpc.yml --parameters file://${params.envitonment}-parameters.json --region 'ap-northeast-1'"
                }
              }
             }
            }
            }
