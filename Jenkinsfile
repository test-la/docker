pipeline {
  agent any
  stages {
    stage('docker') {
      steps {
        sh 'docker run hello-world'
      }
    }

    stage('ps') {
      steps {
        sh 'docker ps'
      }
    }

  }
}