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
            echo "projectname ${projectname}"
          }
        }

        stage('create file') {
          steps {
            writeFile(file: 'testfile', text: 'this is automated file project name ${projectname}')
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

    stage('Archive') {
      steps {
        archiveArtifacts 'testfile'
      }
    }

  }
  environment {
    projectname = 'jenkinspipeline'
  }
}