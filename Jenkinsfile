pipeline {
    agent any 

    stages {
        stage ('verificarDocker'){
            steps {
                sh 'docker info'
            }
        }

        stage ('Docker build'){
            steps {
                sh 'docker-compose up -d'
            }
        }
    }

}