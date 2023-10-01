pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Hello From Blue Ocean'
          }
        }

        stage('Build2') {
          steps {
            echo 'Hello from 2'
          }
        }

        stage('Build3') {
          steps {
            echo 'hello'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Hello From Last Step'
        waitUntil(initialRecurrencePeriod: 10) {
          input 'want to deploy'
        }

      }
    }

  }
}