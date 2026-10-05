pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t myapp .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to Kubernetes'
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }

    }
}
