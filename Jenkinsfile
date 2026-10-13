pipeline{
  agent any
  stages{
    stage('Coding'){
      steps{
        echo 'Start Python Program'
        sh 'python3 --version'
      }
    }
    stage('Testing'){
      steps{
        echo 'Testing the app'
      }
    }
    stage('Deployment'){
      steps{
        echo 'Running python program'
        sh 'python3 app.py'
      }
    }
  }
}
