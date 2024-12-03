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
                sh 'docker build -t abm-lista .'
            }
        }
    }

}