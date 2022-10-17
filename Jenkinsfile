pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/test-la/docker', branch: 'main')
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
            sh 'docker run --name nginx --rm -p 8081:80  -d nginx'
          }
        }

      }
    }

  }
}