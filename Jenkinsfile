pipeline {
agent any 
  stages {
    stage('Build'){
      steps{
        sh 'sudo npm install'
      }
    }
    stage('Deploy'){
      steps{
        sh 'sudo pm2 delete all'
        sh 'sudo pm2 start bin/www'
      }
    }
  
  }
}
