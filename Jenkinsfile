pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        sh 'echo this is "${env.BUILD_NUMBER}"'
        sh 'echo this is ${city}'
      }
    }

  }
  environment {
    city = 'Gotham'
  }
}