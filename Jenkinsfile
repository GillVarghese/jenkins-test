pipeline {
    agent any

    

    
    
    stages {        
             
        stage('Docker Build') {
            
            steps {
                
                    echo 'Docker Build'
                    sh "docker build -t gillvarghesesajan/jenkins-dind:0.0.1 ."
                    sh "docker images"
                
                
            }
            
        }

        stage('Docker Push') {
            
            steps {
                
                    echo 'Docker Push'
                    sh "docker push gillvarghesesajan/jenkins-dind:0.0.1"
        
                
                
            }
            
        }
        
        
    }
}
