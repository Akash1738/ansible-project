pipeline {
    agent any

    stages {

        stage('Clone GitHub Repo') {
            steps {
                git 'https://github.com/Akash1738/ansible-project.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i inventory deploy.yml'
            }
        }
    }
}
