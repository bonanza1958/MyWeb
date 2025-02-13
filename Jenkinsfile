
pipeline {
    agent any
    environment {
        AWS_ACCESS_KEY_ID = credentials('AWS_Credentials') // Reemplaza 'AWS_Credentials' con el ID de tus credenciales
        AWS_SECRET_ACCESS_KEY = credentials('AWS_Credentials')
    }
    stages {
        stage('Deploy to AWS S3') {
            steps {
                script {
                    sh '''
                    aws s3 sync ./dist/ s3://mi-bucket-web --delete
                    '''
                }
            }
        }
    }
}

