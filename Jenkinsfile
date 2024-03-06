pipeline{
  agent any
  stages{
//    stage('Clone repository'){
//      steps{
//        checkout([$class:'GitSCM',
//        branches:[[name: '*/main']],
//       userRemoteConfigs:[[url: 'https://github.com/kushalar03/KushalaR_PES2UG21CS248_Jenkins.git]]])
//     }
//   }
  stage('Build'){
    steps{
      build 'PES2UG21CS248-1'
      sh 'g++ main.cpp -o output'
    }
  }
  stage('Test'){
    steps{
      sh './output'
    }
  }
  stage('Deploy'){
    steps{
      echo 'deploy'
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }  
}
}
