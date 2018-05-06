pipeline {
  agent {
    docker {
      image 'npm:7.0-alpine'
    }

  }
  stages {
    stage('npm install') {
      steps {
        pwd()
        sh 'npm install '
      }
    }
  }
  environment {
    MYVAR = '123'
  }
}