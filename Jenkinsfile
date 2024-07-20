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
                steps { 
                    echo 'Docker Build'
                    sh "docker build -t gillvarghesesajan/sre-interview:0.0.1 ."
                    sh "docker images"
                }
                
            }
            
        }
        
        
    }
}
