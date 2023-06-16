pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build stage"'
      }
    }

    stage('Testing') {
      parallel {
        stage('Testing') {
          steps {
            echo 'Testing '
          }
        }

        stage('Testing with mavan') {
          steps {
            sleep 30
          }
        }

      }
    }

    stage('Staging deploy') {
      steps {
        sleep 30
        echo 'Deploy on staging'
      }
    }

    stage('Prod Deploy') {
      steps {
        sh '''pwd
date
'''
      }
    }

  }
}