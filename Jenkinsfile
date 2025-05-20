pipeline {
    agent any

    environment {
        IMAGE_NAME = 'jenkins-practice-app'
        APP_DIR = 'app' // folder containing Dockerfile, app.py, and requirements.txt
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/mraudacious/jenkins-practice.git'
            }
        }

        stage('Docker Build') {
            steps {
                bat "docker build -t %IMAGE_NAME% .\\%APP_DIR%"
            }
        }

        stage('Docker Run') {
            steps {
                bat "docker run -d -p 5000:5000 %IMAGE_NAME%"
            }
        }

        stage('Linting') {
            steps {
                echo 'Linting step would go here.'
            }
        }

        stage('Install Packages') {
            steps {
                echo 'Install packages step would go here.'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Application is running inside Docker container.'
            }
        }
    }
}