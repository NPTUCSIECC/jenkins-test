pipeline {
  agent any
 
  tools {
    nodejs "localNode"
  }
 
  stages {
    stage('Pull Code'){
      steps{
        sh 'git pull origin develop'
      }
    }
    stage('npm install'){
      steps{
        retry(3){
          sh 'npm i'
        }
      }
    }
    stage('test'){
      steps{
        retry(3){
          sh 'npm test'
        }
      }
    }
  }
}




