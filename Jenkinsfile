


pipeline {
    agent any
    environment{
        CRED=credentials('test')
    }
    

    
    
    stages {        
          stage('SSH') {
            steps {
                echo env.CRED_USR
                
            }
        }         
        
    }
    post{
        always{
            sleep 5
        }
    }
}
