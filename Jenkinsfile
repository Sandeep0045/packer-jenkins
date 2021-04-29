pipeline {
    agent any
    
     environment {
        access_key = ''
        secret_key = 'input_your_secret_key'
    }
    
    
    stages {
        stage('Git Checkout'){
            steps{
                git credentialsId: 'git-id', url: ' https://github.com/Sandeep0045/packer-jenkins.git'
               }

          }
        stage('Build Stages') {
            steps {
                sh 'packer build apache.json'
         }
        } 
       }
     }
