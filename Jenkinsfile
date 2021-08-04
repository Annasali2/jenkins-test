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
    }
}
