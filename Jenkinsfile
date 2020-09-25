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
                sshagent(['123456']) {
                  sh 'ssh -o StrictHostKeyChecking=no -l admin 34.66.141.204 touch test.txt'
                }
            }
        }
    }
}