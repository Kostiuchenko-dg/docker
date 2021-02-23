pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                echo 'Building..'
                dir ('dockerfiles') {
                    sh 'docker build -t maria . '
                }
            }
        }
        stage('Run') {
            steps {
                echo 'Running....'
                sh 'docker run --name mariadb -ti -d -p 3306:3306 maria'
            }
        }
        stage('Test') {
            steps {
                echo 'testing.......'
                sh 'docker ps -a'
            }
        }
        stage('cleanup'){
            steps {
                echo 'stop container mariadb'
                sh 'docker stop mariadb'
                echo 'remove container mariadb'
                sh 'docker rm mariadb'
            }
        }
    }
}