pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/hungpham28197/test-jenkins.git'
                sh 'ssh admin@34.66.141.204 touch test.txt'
            }
        }
    }
}