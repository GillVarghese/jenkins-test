def remote=[:]
remote.name='sonar.avitech-ag.intra'
remote.host='sonar.avitech-ag.intra'
remote.allowAnyHosts=true


pipeline {
    agent any

    environment{
        SSH_CRED=credentials('docker')
    }

    
    
    stages {        
          stage('SSH') {
            steps {
                script{
                    remote.user=env.SSH_CRED_USR
                    remote.password=env.SSH_CRED_PSW
                }
                sshCommand(remote: remote, command: "ls -ltr /home/docker/")
            }
        }         
        
    }
    post{
        always{
            sleep 5
        }
    }
}
