pipeline {
    agent any

    tools {nodejs "NodeJs 20.11.1"}

    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}