pipeline {
    agent any
    stages {
        stage('Clonar Repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/usuario/mi-repo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Compilando el código...'
            }
        }
        stage('Deploy en AWS S3') {
            steps {
                sh 'aws s3 sync . s3://mi-bucket-web --delete'
            }
        }
    }
}


