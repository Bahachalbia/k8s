pipeline {
    agent any
    
    environment {
        DOCKERHUB_CREDENTIALS = credentials('docker_jinkins')
        }
    stages {
     
        stage('login') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u bahachalbia --password-stdin '
               
            }
        }

        stage('push') {
            steps {
                sh "docker push bahachalbia/back:1.0"
            }
        }
        stage('push22') {
            steps {
                sh "docker push bahachalbia/front:latest"
            }
        }

    }
}
