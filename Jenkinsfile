pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                echo 'Checking out source code...'
                git branch: 'main',
               url: 'https://github.com/arunkrishna1296/devops-node-app.git'
                
            }
        }
        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
                
            }
        }
        stage('Test') {
            steps {
               echo 'Running tests...'
                sh 'npm test' 
            }
        }   
        stage('Docker Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t devops-node-app .'
               
            }
        }  
    }
}
