pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                 bat 'docker build -t flask-docker-app .'
            }
        }
        stage('Stop Old Container'){
            steps {
                bat 'docker rm -f flask-container || true'
            }
        }
        stage('Run Container'){
            steps {
                bat 'docker run -d -p 5001:5000 --name flask-container flask-docker-app'
            }
        }
    }
}
