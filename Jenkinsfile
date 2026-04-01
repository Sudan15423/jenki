pipeline {
    agent any

    
	stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Sudan15423/jenki.git',
                    credentialsId: 'git-sudancred01'
            }
        }
        stage('Check Files') {
        steps {
        sh 'ls -ltr'
        sh 'sudp docker ps'
        }
        }
    post {
        success {
            sh 'echo "build successfull"'
        }
        failure {
            sh 'echo "build failed"'
        }
    }
}

