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
	stage('results') {
      junit 'results/*.xml'
    }
  }
}
