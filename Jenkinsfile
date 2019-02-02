pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('UI') {
      parallel {
        stage('Web') {
          steps {
            bat 'runWebTests.bat'
          }
        }
        stage('Mobile') {
          steps {
            bat 'runMobileTests.bat'
          }
        }
      }
    }
  }
  post {
    always {
      junit 'results/*.xml'

    }

  }
}