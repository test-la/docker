pipeline {
    agent any
    triggers {
            pollSCM '*/1 * * * *'
    }
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
