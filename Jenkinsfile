pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/hungpham28197/test-jenkins.git'
            }
        }
    }

     sshagent(['1e949696-12c8-4b78-a0ba-660c59d14d66']) {
                sh 'ssh admin@34.66.141.204 touch test.txt'
    }
}