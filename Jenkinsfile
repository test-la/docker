pipeline {
  agent any
  stages {
    stage('git') {
      environment {
        TOKEN = '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'
      }
      steps {
        sh 'curl -s https://$TOKEN@raw.githubusercontent.com/test-la/docker/main/Dockerfile'
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
            sh 'docker kill nginx'
            sh 'docker run --name nginx --rm -p 8081:80  -d nginx'
          }
        }

      }
    }

  }
}