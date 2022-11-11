pipeline {
    agent any
    stages {
        stage('dockerbuild') {
            steps {
                sh 'sudo docker build -t hello .'
            }
        }
        stage('Execution') {
            steps {
                sh 'sudo docker run hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
