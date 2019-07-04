pipeline {
  agent any
 
  tools {
    nodejs "localNode"
  }
 
  stages {
    stage('Pull Code'){
      steps{
        sh 'git pull'
      }
    }
    stage('Test'){
      steps{
        retry(3){
          sh ''' 
            npm i
            npm test
          '''
        }
      }
    }
  }
}
