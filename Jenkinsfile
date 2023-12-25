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
            sh 'cd app'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f app/Dockerfile .'
      }
    }

  }
}