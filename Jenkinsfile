pipeline {
  agent any
  stages {
    stage('step-1') {
      parallel {
        stage('step-1') {
          steps {
            echo 'qwerty'
            echo 'asdf'
          }
        }

        stage('step-1.1') {
          steps {
            sh 'ps '
            echo 'step 1.1'
          }
        }

        stage('step-1.2') {
          steps {
            sh 'hostname'
            echo 'step 1.2'
          }
        }

      }
    }

    stage('step 2') {
      parallel {
        stage('step 2') {
          steps {
            sh 'sleep 30'
          }
        }

        stage('step 2.1') {
          steps {
            sh 'sleep 35'
          }
        }

        stage('step 2.2') {
          steps {
            sh 'sleep 48'
          }
        }

      }
    }

    stage('last') {
      steps {
        sleep 2
      }
    }

  }
  environment {
    key1 = 'val1'
    key2 = 'val2'
  }
}