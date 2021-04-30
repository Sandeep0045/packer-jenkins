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
                sh  'packer build  apache.json'                   
         }
        } 
       }
     }

