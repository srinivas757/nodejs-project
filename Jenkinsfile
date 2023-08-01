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
        sh 'docker stop srinivas'
        sh 'docker rm srinivas'
        sh 'docker run -itd -p 3000:3000 --name srinivas srinivas:$BUILD_NUMBER'
      }
    }
  
  }
}
