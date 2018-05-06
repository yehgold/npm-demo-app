pipeline {
  agent {
    docker {
      image 'publicisworldwide/jenkins-slave'
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