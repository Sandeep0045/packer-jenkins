pipeline {
    agent any
    
    
    stages {
        stage('Git Checkout'){
            steps{
                git credentialsId: 'git-id', url: ' https://github.com/Sandeep0045/packer-jenkins.git'
               }

          }
        stage('Build Stages') {
            steps {
                script {
                  withCredentials([file(credentialsId: 'my-key', variable: ' SSH_PRIVATE_KEY')]) {
                      sh """
                        packer build   apache.json'
                       """
                                        
           }                             
         }
        } 
       }
     }
