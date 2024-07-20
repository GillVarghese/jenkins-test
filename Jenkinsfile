pipeline {
    agent any

        stage('Docker Run') {
            
            steps {
                
                    echo 'Docker Run'
                    sh "ansible-playbook -i TestProject-inventory playbook.yml"

            }
            
        }
        
    
}
