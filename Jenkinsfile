pipeline {
    agent any
    stages {
        stage('SSH') {
            steps {
                sshagent(['1234']) {
                  sh 'ssh root 202.92.6.130 touch test.txt'
                }
            }
        }
    }
}