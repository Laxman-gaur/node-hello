pipeline {
    agent any
   
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('approve') {
            steps {
                input 'kindly approve for this deployment'
            }
        }

        stage('deploy') { 
            steps {
                sh 'pm2 start /node-hello/node-hello.js' 
            }
        }
    }
}
