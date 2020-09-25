pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                sshagent(['123456']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l admin 34.66.141.204 touch test.txt'
                }
            }
        }
    }
}