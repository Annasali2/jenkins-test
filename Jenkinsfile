pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                    sh' npm build'
                } 
            }
        }
        stage('Host') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm start'
                } 
            }
        }
    }
}
