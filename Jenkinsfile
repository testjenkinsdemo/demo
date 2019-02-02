pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('WebTestsxxx') {
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