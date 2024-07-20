pipeline {
    agent any

    

    
    
    stages {        
        stage('Checkout') {
            steps {
                echo 'Checkout' 
                checkout scm
            }
        }        
        stage('Docker Build') {
            
            steps {
                script {
                    app = docker.build("gillvarghesesajan/sre-interview:0.0.1")
                }
                
            }
            
        }
        
        
    }
}
