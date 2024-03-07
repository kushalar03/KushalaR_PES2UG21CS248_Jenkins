pipeline {
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES2UG21CS248-1'
        sh 'g++ PES2UG21CS248.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'eploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
