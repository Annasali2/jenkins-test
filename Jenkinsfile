pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                    sh 'npm build'
                } 
            }
        }
        stage('building image') {
            agent {
                docker { dockerfile true }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
