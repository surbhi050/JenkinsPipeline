pipeline {
  agent {
  dockerfile true
  }
  stages {
    
        stage('Build') {
          steps {
            echo 'build stage'
            sh 'java -version'
          }
        }

        stage('test stage') {
          steps {
            echo 'testing phase'
            echo "projectname ${projectname}"
          }
        }

       
}
}
