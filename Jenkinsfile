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
            echo "projectname $projectname"
          }
        }

      }
    }

    stage('Deployment phase') {
      steps {
        input(message: 'please provide approval for deployment', id: 'Ok')
        echo 'deployment phase'
      }
    }

  }
  environment {
    projectname = 'jenkinspipeline'
  }
}