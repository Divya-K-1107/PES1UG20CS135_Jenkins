pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ -o task5 task5.cpp'
        build job: 'PES1UG20CS135-1'
      }
    }
    stage('Test'){
      steps{
        sh './task5'
        sh 'exit 1'//error
    
      }
    }
   stage('Deploy'){
      steps{
        echo 'Deploying'
        
      }
    }
  }
  post{
    failure{
      echo 'pipeline failed'
    }
  }
}
