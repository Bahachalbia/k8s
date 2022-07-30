pipeline {
    agent any 
    stages {
        stage('install client depondances') {
            steps {
                sh "cd client && npm install"
            }
        }
        stage('install server depondance') {
            steps {
                sh "cd .."
                sh "cd server && npm install"  
            }
        }
    }
}