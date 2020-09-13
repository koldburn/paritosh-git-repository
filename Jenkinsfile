pipeline {
  agent any
  stages {
    stage('Fluffy Build') {
      steps {
        sh 'echo this is build > batman_build.txt'
        stash(name: 'batsy', includes: 'batman_build.txt')
      }
    }

    stage('Fluffy Test') {
      parallel {
        stage('TestA') {
          steps {
            sh 'echo this is test > batman_test.txt'
            dir(path: 'batsy') {
              unstash 'batsy'
            }

            sh 'cat batsy/batman.txt'
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