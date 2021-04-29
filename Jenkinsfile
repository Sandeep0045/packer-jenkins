pipeline {
    agent any
    
    
    stages {
        stage('Git Checkout'){
            steps{
                git credentialsId: 'git-id', url: ' https://github.com/Sandeep0045/packer-jenkins.git'
               }

          }
        stage('Build Stages') {
    environment {
      AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
      AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }       
            steps {
                sh 'packer build -var AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID') -var       AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY') apache.json'
         }
        } 
       }
     }
