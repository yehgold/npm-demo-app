pipeline {
  agent {
    docker {
      image 'mkenney/npm:7.0-alpine'
      args 'git clone https://github.com/leonjalfon1/nodejs-demoapp.git && cd nodejs-demoapp && npm install'
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