pipeline {
    agent {
        docker { image 'node:16.13.1-alpine' }
    }
    stages {
         stage('Test') {
            steps {
                sh 'node --version'
            }
        }
        stage('build') {
            steps {
               echo '*****************START********************'
               sh 'npm install'
               echo '*****************FINAL********************'
            }
        }
        stage('run test'){
            steps{
                sh 'npx wdio run wdio.conf.js'
            }
        }
    }
}
