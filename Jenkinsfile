pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/jazersalazar/docker-test', branch: 'dev')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Unit Test') {
          steps {
            sh '''cd app
'''
            sh '''npm i
'''
            sh 'npm run test:unit'
          }
        }

      }
    }

  }
}