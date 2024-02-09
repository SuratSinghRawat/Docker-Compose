pipeline {
    agent {label 'docker_server'}
    stages {
        stage('verify tools'){
            steps{
             sh '''
                docker version
                docker info
                docker compose version
             '''
            }
        }
        stage('deploy images'){
            steps{
                sh 'docker-compose up'
            }
        }
    }
}