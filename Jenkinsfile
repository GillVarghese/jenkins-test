pipeline {
    agent any

    stages {        
  
        stage('Docker Version') {
            
            steps {
                sh "docker -v"
                
            }
        }
        stage('Docker Build') {
            
            steps {
                sh "docker build ."
                
            }
        }
        stage('Docker Image check') {
            
            steps {
                sh "docker images"
                
            }
        }
    }
}
