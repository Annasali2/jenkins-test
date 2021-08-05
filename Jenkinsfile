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
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
