pipeline {
    agent any
    stages {
        stage ('test') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
            }
        }
        stage('SSH') {
            steps {
                sshagent(['123456']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l admin 34.66.141.204 touch test.txt'
                }
            }
        }
    }
}