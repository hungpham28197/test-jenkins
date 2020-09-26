pipeline {
    agent any
    stages {
        stage ('test') {
            steps {
                withMaven(jdk: 'java', maven: 'Maven') {
                    sh 'mvn clean install' 
                }
            }
        }
        stage('SSH') {
            steps {
                sshagent(['1234']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l root 202.92.6.130 touch test.txt'
                }
            }
        }
    }
}