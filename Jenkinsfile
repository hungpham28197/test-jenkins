pipeline {
    agent any
    stages {
        stage('SSH') {
            steps {
                sshagent(['1234']) {
                  sh 'ssh -p 24700 root 202.92.6.130 touch test.txt'
                }
            }
        }
    }
}