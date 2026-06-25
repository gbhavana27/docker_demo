pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                 git branch: 'main',
                    url: 'https://github.com/gbhavana27/docker_demo.git'
            }
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8090:80 web-image-app'
            }
        }
    }
}