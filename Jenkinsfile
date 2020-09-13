pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        sh 'echo this is build > batman_build.txt'
      }
    }

    stage('Fluffy Test') {
      parallel {
        stage('TestA') {
          steps {
            sh 'echo this is test > batman_test.txt'
          }
        }

        stage('TestB') {
          steps {
            sh '''sleep 10
echo done.'''
          }
        }

      }
    }

    stage('Fluffy Deploy') {
      steps {
        sh 'echo this is deploy > batman_deploy.txt'
      }
    }

  }
}