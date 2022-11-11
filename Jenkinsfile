pipeline {
    agent any
    stages {
        stage('dockerbuild') {
            steps {
                script{
                    sh 'docker build .'
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
