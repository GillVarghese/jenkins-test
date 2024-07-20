pipeline {
    agent any

    /*parameters {
        string(name: 'NAME', description: 'Please tell me your name')
        choice(name: 'GENDER', choices: ['Male', 'Female'], description: 'Choose Gender')
    }*/

    environment {
        NAME = 'Gill'
        GENDER    = 'Male'
        DOCKER_CRED = credentials('docker_hub') 
        PRODUCT = 'jenkins-pipeline-tutorial'
        GIT_HOST = 'github.com'
        GIT_OWNER = 'GillVarghese'
    }
    
    stages {        
        stage('Checkout') {
            steps {
                echo 'Checkout' 
                checkout scm
            }
        }        
        stage('Docker Build') {
            /*steps { 
                echo 'Docker Build'
                sh "docker build -t gillvarghesesajan/sre-interview:0.0.1 ."
                sh "docker images"
            }*/
            steps {
                script {
                    app = docker.build("gillvarghesesajan/sre-interview:0.0.1")
                }
                
            }
            
        }
        stage('Docker Publish') {
            /*when{
                allOf{
                    environment name: 'username', value: 'gill';
                    environment name: 'password', value: 'gill'                   
                }
            }*/
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker_hub') {
                        app.push()
                    }
                }
                
            }
            
        }
        
    }
}
