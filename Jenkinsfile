pipeline {
    agent any
     environment { 

        AWS_ACCESS_KEY_ID     = credentials('Access_key_ID')
        AWS_SECRET_ACCESS_KEY = credentials('Secret_access_key')

    }
    
    
    stages {
            stage('git pull') {
            steps {
                sh " git pull https://github.com/manaralolasi/coding.git "
            }
        }
        stage('create stack') {
            steps {
                sh " aws cloudformation create-stack --stack-name duihua2-cloudfront --template-body file://CloudFront.yml --region 'us-east-2'"
            }
        }
    }
}
