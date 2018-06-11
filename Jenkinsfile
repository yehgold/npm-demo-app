pipeline {
  agent {
    docker {
      image 'node'
    }

  }
  stages {
    stage('npm install') {
      agent any
      steps {
        sh 'npm install'
      }
    }
    stage('npm test1') {
      parallel {
        stage('test 1') {
          agent any
          steps {
            sh 'npm run test'
          }
        }
        stage('test 2') {
          agent any
          steps {
            sh 'npm run test'
          }
        }
        stage('test 3') {
          agent any
          steps {
            sh 'npm run test'
          }
        }
      }
    }
    stage('docker build') {
      agent any
      steps {
        sh 'echo docker build -t myapp .'
      }
    }
    stage('docker push') {
      agent any
      steps {
        sh 'echo pushed'
      }
    }
    stage('deploy env1') {
      parallel {
        stage('deploy env1') {
          agent any
          steps {
            sh 'echo deployed env1'
          }
        }
        stage('deploy env2') {
          agent any
          steps {
            sh 'echo deployed env2'
          }
        }
        stage('deploy env3') {
          agent any
          steps {
            sh 'echo deployed env3'
          }
        }
      }
    }
    stage('notification') {
      agent any
      steps {
        mail(subject: 'build end', body: 'build end', from: 'jenkins@blueocean.com', to: 'leonj@sela.co.il', replyTo: 'leonj@sela.co.il')
      }
    }
  }
}