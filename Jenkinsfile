pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                echo 'Building..'
                dir ('dockerfiles') {
                    sh 'docker build . '
                }
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