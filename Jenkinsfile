pipeline {
    agent any

    environment {
        IMAGE_NAME = "minfy-app"
        TAG = "latest"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    echo "Building Docker image..."
                    sh 'docker build -t $IMAGE_NAME:$TAG .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    echo "Running Docker container..."
                    sh 'docker run --rm $IMAGE_NAME:$TAG'
                }
            }
        }
    }
}
