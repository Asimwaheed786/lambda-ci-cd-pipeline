pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Asimwaheed786/lambda-ci-cd-pipeline.git'
            }
        }
        stage('Deploy to Lambda') {
            steps {
                script {
                    sh '''
                    aws lambda update-function-code --function-name BackupAutomation \
                        --zip-file fileb://function.zip
                    '''
                }
            }
        }
    }
}
