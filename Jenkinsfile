pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/hungpham28197/test-jenkins.git'
                sh 'mvn -v'
                sh 'java -v'
            }
        }
    }
}