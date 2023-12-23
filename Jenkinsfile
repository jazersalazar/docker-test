pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/jazersalazar/docker-test', branch: 'dev')
      }
    }

  }
}