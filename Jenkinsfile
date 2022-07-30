pipeline {
    environment {
        DOCKERHUB_CREDENTIALS_LOCAL = credentials("DOCKERHUB_CREDENTIALS")

    }
    agent any 
    stages { 
        
        /*stage('test') {
            steps { 
                sh 'echo $DOCKERHUB_CREDENTIALS_LOCAL_USR' 
                sh 'echo $DOCKERHUB_CREDENTIALS_LOCAL_PSW'
            }
        }*/
        stage('Docker build client') {
            steps {
                sh 'cd client'
                sh 'docker build -t bouregbaslah/memoriesui:latest .'
            }
        }
        /*stage('Docker build') {
            steps {
                sh 'docker-compose up -f --no-color -d --wait'
                sh 'docker-compose ps'
                echo 'Docker-compose-build Build Image Completed'
            }
        }
        stage('Login to Docker Hub') {          
           steps{                          
                sh 'echo $DOCKERHUB_CREDENTIALS_LOCAL_PSW | docker login -u $DOCKERHUB_CREDENTIALS_LOCAL_USR --password-stdin'                     
                echo 'Login Completed'      
            } 
        }*/    
        /*stage('Push Image to Docker Hub') {         
           steps{                            
               sh 'sudo docker push <dockerhubusername>/<dockerhubreponame>:$BUILD_NUMBER'           
               echo 'Push Image Completed'       
         } */         
}
}