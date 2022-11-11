pipeline {
    agent any
    stages {
        stage('dockerbuild') {
            steps {
                docker.build("https://github.com/test-la/docker/Dockerfile")
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
