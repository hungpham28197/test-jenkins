pipeline {
    agent any

    tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
    }

    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

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