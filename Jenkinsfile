pipeline {
    agent any

    

    
    
    stages {        
             
        stage('Docker Build') {
            
            steps {
                
                    echo 'Docker Build'
                    sh "ansible-playbook -i TestProject-inventory playbook.yml"
                
                
            }
            
        }
        
    }
}
