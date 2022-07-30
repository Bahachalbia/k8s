pipeline {
    agent any 
    stages {
        stage('install client depondance') {
            steps {
                sh "cd client"
                sh "npm install"  
            }
        }
        stage('install server depondance') {
            steps {
                sh "cd .."
                sh "cd server"
                sh "npm install"  
            }
        }
    }
}