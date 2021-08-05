pipeline {
    agent any
    stages {
        stage('Host') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                    sh' npm start'
                    sh' npm build'
                } 
            }
        }
    }
}
