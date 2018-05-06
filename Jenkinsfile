pipeline {
  agent any
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