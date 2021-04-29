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
                sh 'packer build -var \"access_key=${access_key}\"  -var \"access_key=${secret_key}\" apache.json'
         }
        } 
       }
     }
