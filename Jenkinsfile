pipeline {
  agent {
    docker {
      image 'node'
    }

  }
  stages {
    stage('npm install') {
      agent {
        docker {
          image 'node'
        }

      }
      steps {
        sh 'npm install'
      }
    }
    stage('npm test1') {
      parallel {
        stage('test 1') {
          agent {
            docker {
              image 'node'
            }

          }
          steps {
            sh 'npm run test'
          }
        }
        stage('test 2') {
          agent {
            docker {
              image 'node'
            }

          }
          steps {
            sh 'npm run test'
          }
        }
        stage('test 3') {
          agent {
            docker {
              image 'node'
            }

          }
          steps {
            sh 'npm run test'
          }
        }
      }
    }
    stage('docker build') {
      agent {
        docker {
          image 'docker'
        }

      }
      steps {
        sh 'docker build -t myapp .'
      }
    }
    stage('docker push') {
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
      steps {
        mail(subject: 'build end', body: 'build end', from: 'jenkins@blueocean.com', to: 'leonj@sela.co.il', replyTo: 'leonj@sela.co.il')
      }
    }
  }
}