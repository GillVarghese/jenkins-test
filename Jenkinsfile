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
                
                    echo 'Docker Build'
                    ansiblePlaybook installation: 'ansible', inventory: './TestProject-inventory', playbook:'./playbook.yml'
                
                
            }
            
        }
        
    }
}
