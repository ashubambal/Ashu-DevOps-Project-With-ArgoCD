pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Stage'
        sh 'uptime'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test Stage'
            sh 'top'
          }
        }

        stage('Monitor') {
          steps {
            echo 'Monitor Stage'
            sh 'df -h'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy Code'
        sh 'date'
      }
    }

  }
}