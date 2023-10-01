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

        stage('') {
          steps {
            git(url: 'https://github.com/yoyoraso/privetrepo.git', branch: 'main', credentialsId: '25c0135d-dca3-4578-a7ca-78126b36d242')
            sh 'cat test.txt'
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