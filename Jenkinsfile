pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t vaishnavijp/devops-node-app:1.0 ./app'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push vaishnavijp/devops-node-app:1.0'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                kubectl apply -f terraform/deployment.yaml
                kubectl apply -f terraform/service.yaml
                '''
            }
        }

    }
}