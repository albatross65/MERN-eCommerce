pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Getting the latest code from GitHub...'
                checkout scm
            }
        }

        stage('Build Backend Image') {
            steps {
                echo 'Building backend Docker image...'
                sh 'docker build -t mern-backend -f backend/Dockerfile .'
            }
        }

        stage('Build Frontend Image') {
            steps {
                echo 'Building frontend Docker image...'
                sh 'docker build -t mern-frontend ./frontend'
            }
        }

        stage('Done') {
            steps {
                echo 'Build pipeline completed successfully!'
            }
        }
    }
}