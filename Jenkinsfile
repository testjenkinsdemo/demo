pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('test') {
      steps {
        bat 'run.bat'
      }
    }
  }
  post {
    always {
      archive 'results/*.html'
      junit 'results/*.xml'

    }

  }
}
