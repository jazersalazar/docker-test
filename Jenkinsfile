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

        stage('') {
          steps {
            sh 'cd app && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}