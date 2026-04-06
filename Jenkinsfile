pipeline {
    agent any
    
    environment {
        DOCKER_BUILDKIT = '1'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mostafaanwar862004/docker-react -f Dockerfile.dev .'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'docker run -e CI=true mostafaanwar862004/docker-react npm run test'
            }
        }
    }
}