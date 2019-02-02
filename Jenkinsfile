pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('UI Tests') {
      parallel {
        stage('WebTests') {
          steps {
            bat 'runWebTests.bat'
          }
        }
        stage('Mobile Tests') {
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