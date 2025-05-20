pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Banafsha12/Devops_Proj.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops_proj .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 3000:3000 devops_proj'
            }
        }
    }
}
