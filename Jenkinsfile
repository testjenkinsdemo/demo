pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('Mobile Tests') {
      steps {
        bat 'runMobileTests.bat'
      }
    }
  }
  post {
    always {
      junit 'results/*.xml'

    }

  }
}