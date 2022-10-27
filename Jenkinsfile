pipeline {
    agent any

    stages {
        stage('Docker build and push') {
            steps {
                sh 'docker-compose build'
                sh 'docker-compose push'
            }
        }
        stage('deploy') {
            steps {
                sh 'docker stack deploy --compose-file docker-compose.yaml teststack'
            }
        }
    }
}