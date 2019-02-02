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
	steps {
      junit 'results/*.xml'
	  }
    }
  }
}
