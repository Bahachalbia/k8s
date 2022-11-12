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
                withDockerRegistry([ credentialsId: "docker_jinkins", url: "" ]) {
                    bat "docker push bahachalbia/front:latest"
               } 
            }
        }
        stage('push22') {
            steps {
                sh "docker push back:latest"
            }
        }

    }
}
