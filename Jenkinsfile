pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
      }
    }
    stage('Web Tests') {
      steps {
        bat 'run.bat'
      }
    }
    stage('Mobile Tests') {
      steps {
        echo 'hh'
      }
    }
  }
  post {
    always {
      junit 'results/*.xml'

    }

  }
}