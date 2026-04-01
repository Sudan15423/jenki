pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
                sh 'rm -Rf jenki'
                sh 'git clone https://github.com/Sudan15423/jenki.git'
                sh 'pwd'
                sh 'ls -ltr'
            }
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

