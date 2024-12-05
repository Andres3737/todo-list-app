pipeline {
    agent any 

    stages {
        stage ('verificarDocker'){
            steps {
                sh 'docker info'
            }
        }

        stage ('verificar docker-compose'){
            steps {
                sh 'cat docker-compose.yml'
            }
        }

        stage ('Docker build'){
            steps {
                sh 'docker-compose up --build -d'
            }
        }
    }

    post {
        success {
            slackSend(channel: '#jenkins', message: 'Todo bien')

        }

        failure {
            slackSend(channel: '#jenkins', message: 'Algo anda mal')


        }
    }

}