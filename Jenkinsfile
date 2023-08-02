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
        sh '''
          sudo docker stop srinivas
          sudo docker rm srinivas
        '''
        sh 'sudo docker run -itd -p 3000:3000 --name srinivas srinivas:$BUILD_NUMBER'
        
      }
    }
  
  }
}
