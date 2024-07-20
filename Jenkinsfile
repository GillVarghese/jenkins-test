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
                app = docker.build("gillvarghesesajan/jenkins-dind:0.0.1")
                
            }
        }
        stage('Docker Image check') {
            
            steps {
                sh "docker images"
                
            }
        }
    }
}
