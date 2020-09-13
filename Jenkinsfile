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
            dir(path: 'batsybuild') {
              unstash 'batsy'
            }

            sh 'cat batsybuild/batman_build.txt'
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

    stage('GiveInput') {
      steps {
        input(message: 'can we proceed', ok: 'yea, go on dude')
      }
    }

    stage('Fluffy Deploy') {
      steps {
        echo 'this is deploy step'
      }
    }

  }
}