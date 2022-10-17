pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/test-la/docker', branch: 'main')
      }
    }

    stage('error') {
      steps {
        sh 'ls -la'
      }
    }

  }
}