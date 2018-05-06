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
        sh '''ls
yum install -y nodejs npm
npm install
'''
      }
    }
  }
  environment {
    MYVAR = '123'
  }
}