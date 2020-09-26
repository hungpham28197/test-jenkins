pipeline {
    agent any
    stages {
        stage('SSH') {
            steps {
                sshagent(['1234']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l root 202.92.6.130 touch test.txt'
                }
            }
        }
    }
}