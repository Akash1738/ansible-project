pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Akash1738/ansible-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t banking-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop banking-container || true'
                sh 'docker rm banking-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name banking-container -p 3000:3000 banking-app'
            }
        }
    }
}

