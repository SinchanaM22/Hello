pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'javac Hello World.java'
            }
        }
        stage('Run'){
            steps {
                bat 'java HelloWorld'
            }
        }
    }
}
