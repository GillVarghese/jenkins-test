def remote=[:]
remote.name='sonar.avitech-ag.intra'
remote.host='sonar.avitech-ag.intra'
remote.allowAnyHosts=true


pipeline {
    agent any

    

    
    
    stages {        
          stage('SSH') {
            steps {
                script{
                    remote.user='docker'
                    remote.password='avitech'
                }
                sshCommand(remote: remote, command:"docker ps -a")
            }
        }         
        
    }
    post{
        always{
            sleep 5
        }
    }
}
