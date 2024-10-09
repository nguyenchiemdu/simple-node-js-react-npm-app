pipeline {
    agent any

    tools {nodejs "NodeJs 20.11.1"}

    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
                sh 'npm i -g pm2'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
         stage('Deliver') {
            steps {
                sh 'pm2 status'
                sh 'pm2 start'
            }
        }
    }
}