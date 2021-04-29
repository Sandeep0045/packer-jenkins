pipeline {
    agent any
    
     environment {
        aws_access_key = credentials('aws_access_key')
        aws_secret_key = credentials('aws_secret_key')
    }
    
    
    stages {
        stage('Git Checkout'){
            steps{
                git credentialsId: 'git-id', url: ' https://github.com/Sandeep0045/packer-jenkins.git'
               }

          }
        stage('Build Stages') {
            steps {
                sh 'ls -la; pwd;packer build apache.json'
         }
        } 
       }
     }
