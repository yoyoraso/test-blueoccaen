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
            echo 'Hello 2'
          }
        }

        stage('Build3') {
          steps {
            echo 'Build3'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Hello From Test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Hello From Last Step'
      }
    }

  }
}