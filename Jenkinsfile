pipeline {
    agent any
    stages {
        stage('Image Build') {
            agent { dockerfile true }
            steps {
                sh 'node --version'
            }
        }
        stage('Host') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                    sh' npm build'
                    sh' npm start'
                } 
            }
        }
    }
}
