pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        sh 'echo this is ${env.BUILD_NUMBER}'
      }
    }

  }
  environment {
    city = 'Gotham'
  }
}