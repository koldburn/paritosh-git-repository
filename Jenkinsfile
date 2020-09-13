pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        sh 'echo this is ${env.city}'
      }
    }

  }
  environment {
    city = 'Gotham'
  }
}