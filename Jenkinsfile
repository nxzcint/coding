pipeline {
    agent any
     environment { 

        AWS_ACCESS_KEY_ID     = credentials('Access_key_ID')
        AWS_SECRET_ACCESS_KEY = credentials('Secret_access_key')

    }
    stages {
        stage('create stack') {
            steps {
                sh " aws cloudformation create-stack --stack-name duihua-cloudfront --template-body file://CloudFront.yml --region 'us-east-2'"
            }
        }
    }
}
