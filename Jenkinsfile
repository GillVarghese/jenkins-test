pipeline {
    agent any

    

    
    
    stages {        
             
        stage('Docker Build') {
            
            steps {
                
                    echo 'Docker Build'
                    ansiblePlaybook installation: 'ansible' inventory: './TestProject-inventory' playbook:'./playbook.yml'
                
                
            }
            
        }
        
    }
}
