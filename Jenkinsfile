pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(branch: 'master', url: 'https://github.com/johan974/robot-framework-demo1.git')
      }
    }
    stage('Test') {
      steps {
        sh 'echo ${PWD}'
      }
    }
  }
  post {
    always {
      archive 'reports/*.html'

    }

  }
}