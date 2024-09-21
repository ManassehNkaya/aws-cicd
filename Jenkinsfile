pipeline {
 agent any 

 environment {
    BRANCH_NAME = 'main'
    GIT_URL = 'https://github.com/ManassehNkaya/aws-cicd.git'
 }
  
  stages {
   stage('git checkout'){
    steps{
        git branch: 'main', "${BRANCH_NAME}", url: "${GIT_URL}"
    }
   }
   stage('docker build'){
    steps{
        sh 'docker build -t aws-cicd .'
        sh 'docker images'
    }
   }
  }
}