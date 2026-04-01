pipeline {
    agent any

    stages {
        stage('Remove Cloned Code') {
            steps {
                
                sh 'rm -Rf proj-feb'
            }
        }

        stage('Remove Docker Images') {
            steps {
                
                sh 'sudo docker rmi susigugh/blog:17-Jul || true'
                
                
                sh 'sudo docker rmi blog || true'
            }
        }

        stage('Prune System') {
            steps {
                
                sh 'sudo docker builder prune -f'
            }
        }
    }
}
