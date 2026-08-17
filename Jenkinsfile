pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
                
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
        echo 'Testing application...'
        sh 'node --check app.js'
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
