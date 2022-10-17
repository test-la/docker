pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        sh 'wget https://github.com/test-la/docker/blob/main/Dockerfile'
      }
    }

    stage('dockerbuild') {
      parallel {
        stage('dockerbuild') {
          steps {
            sh 'docker build .'
          }
        }

        stage('Nginx') {
          steps {
            sh 'docker run nginx -d'
          }
        }

      }
    }

  }
}