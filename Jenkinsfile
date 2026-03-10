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

        stage('Deploy to EC2') {
            steps {
                sshagent(['ec2-ssh-key']) {
                    sh '''
                    ssh -o StrictHostKeyChecking=no ubuntu@43.204.102.121 '
                    sudo docker stop devops-container || true
                    sudo docker rm devops-container || true
                    sudo docker pull vaishnavijp/devops-node-app:1.0
                    sudo docker run -d -p 80:3000 --name devops-container vaishnavijp/devops-node-app:1.0
                    '
                    '''
                }
            }
        }

    }
}