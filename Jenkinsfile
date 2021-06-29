pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'build stage'
          }
        }

        stage('test stage') {
          steps {
            echo 'testing phase'
          }
        }

      }
    }

    stage('Deployment phase') {
      steps {
        echo 'deployment phase'
      }
    }

  }
  environment {
    testing = ''
  }
}