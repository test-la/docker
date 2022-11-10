pipeline {
    agent any
    triggers {
            pollSCM '*/1 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Prueba de build después de agregar el pollSCM..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
