pipeline {
    agent any
    triggers {
            pollSCM '*/1 * * * *'
    }
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
