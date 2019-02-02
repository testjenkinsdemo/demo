pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('WebTests') {
      steps {
        bat 'runWebTests.bat'
      }
    }
  }
  post {
    always {
      junit 'results/*.xml'

    }

  }
}