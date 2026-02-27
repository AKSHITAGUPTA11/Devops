pipeline {
    agent any
    
    stages {
        
        stage ('Git-Pull') {
            steps {
               git branch: 'main', url: 'https://github.com/AKSHITAGUPTA11/EasyCRUD.git'
            }
        }
         stage ("Docker--Backend-Build") {
            steps {
                sh '''
                cd backend
                docker build -t akshitagupta/easy-backend:latest .'''
            }
        }
        stage ("Docker-Frontend-Build") {
            steps {
                sh '''
                pwd
                cd frontend
                docker build -t akshitagupta/easy-frontend:latest .'''
            }
        }
         stage ("Docker-Push") {
            steps {
               sh '''
                docker push akshitagupta/easy-backend:latest
                docker push akshitagupta/easy-frontend:latest '''
            }
        }
         stage ("Deploy") {
            steps {
                sh 'kubectl apply -f simple-deploy/. '
            }
        }
        
    }
    
}
