pipeline {
    agent any
    environment { 
        registry = "annastkxel/getting-started" 
        registryCredential = 'boogeytkxel' 
        dockerImage = '' 
    }
    stages {
        stage('Host') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                    sh' npm build'
                } 
            }
        }
        stage('Cloning our Git') { 
            steps { 
                git 'https://github.com/Annasali2/jenkins-test.git' 
            }
        } 
        stage('Building our image') { 
            steps { 
                script { 
                    dockerImage = docker.build registry + ":$BUILD_NUMBER" 
                }
            } 
        }
    }
}
