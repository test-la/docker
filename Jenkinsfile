pipeline {
    agent any
    stages {
        stage('dockerbuild') {
            steps {
                script{
                    sh 'docker build -t test .'
                    sh 'docker run -d -t test test'
                    sh 'docker export --output="test.tar" test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
