pipeline {
  agent {
    docker {
      image 'mkenney/npm'
    }

  }
  stages {
    stage('npm install') {
      steps {
        sh 'npm install '
      }
    }
  }
  environment {
    MYVAR = '123'
  }
}