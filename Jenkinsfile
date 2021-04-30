pipeline {
    agent any
    environment {
        aws_access_key = "${AWS_KEY}"
        aws_secret_key = "${AWS_SECRET}"

        
    
    
    
    stages {
        stage('Git Checkout'){
            steps{
                git credentialsId: 'git-id', url: ' https://github.com/Sandeep0045/packer-jenkins.git'
               }

          }
        stage('Build Stages') {
            steps {
                sh  'packer build  -var \"aws_access_key=${AWS_KEY}\" -var \"aws_secret_key =${AWS_SECRET}\" apache.json'                   
         }
        } 
       }
     }
}
