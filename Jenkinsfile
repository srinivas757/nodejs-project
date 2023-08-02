pipeline {
agent any
  stages {
    stage('Build'){
      steps{
        sh 'sudo docker build -t srinivas:$BUILD_NUMBER .'
      }
    }
    stage('Deploy'){
      steps{
        sh 'sudo docker run -itd -p 3000:3000 srinivas:$BUILD_NUMBER'
        
      }
    }
  
  }
}
