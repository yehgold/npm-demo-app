pipeline {
  agent any
  stages {
    stage('npm install') {
      parallel {
        stage('npm install') {
          steps {
            pwd()
            sh 'ls'
            sh 'ls'
          }
        }
        stage('1') {
          steps {
            sh 'ls'
          }
        }
        stage('2') {
          steps {
            sh 'echo hello'
          }
        }
      }
    }
    stage('') {
      steps {
        sh 'ls'
        sh 'pwd'
      }
    }
  }
  environment {
    MYVAR = '123'
  }
}