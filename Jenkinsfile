pipeline {
    agent any
    stages {
        stage('dockerbuild') {
            steps {
                sh 'docker build -t hello .'
            }
        }
        stage('Execution') {
            steps {
                sh 'docker run hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
