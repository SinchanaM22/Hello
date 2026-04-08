pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-docker-app .'
            }
        }
        stage('Stop Old Container'){
            steps {
                sh 'docker rm -f flask-container || true'
            }
        }
        stage('Run Container'){
            steps {
                sh 'docker run -d -p 5001:5000 --name flask-container flask-docker-app'
            }
        }
    }
}
