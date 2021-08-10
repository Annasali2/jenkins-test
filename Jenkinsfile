pipeline {
    agent any
    environment { 
        registry = "annastkxel/getting-started" 
        registryCredential = 'boogeytkxel' 
        dockerImage = '' 
    }
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
                } 
            }
        }
        stage('Host') {
            steps {
                nodejs('NodeJS'){
                    sh 'node sonarqube-scanner.js'
                } 
            }
        }
    }
}
