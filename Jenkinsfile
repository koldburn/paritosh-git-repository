pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        echo 'i am batman build'
        sh 'echo Another Build!!'
      }
    }

    stage('Fluffy Test') {
      steps {
        echo 'i am batman test'
        sleep 3
        sh 'echo success!'
      }
    }

    stage('Fluffy Deploy') {
      steps {
        echo 'i am batman deploy'
      }
    }

  }
}