pipeline {
    agent any

    stages {

        stage('Pull Code') {
            steps {
                git branch: 'main',
                    url: 'YOUR_GITHUB_REPOSITORY_URL'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t docker-demo:latest .'
            }
        }

        stage('Display Image Details') {
            steps {
                bat 'docker images docker-demo'
            }
        }
    }
}