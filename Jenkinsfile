pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/axdhi7/amazon-clone.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install --prefix backend'
                sh 'npm install --prefix frontend'
            }
        }
        
        stage('Build Frontend') {
            steps {
                sh 'npm run build --prefix frontend'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test --prefix backend'
                sh 'npm test --prefix frontend'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                // Add deployment steps if needed
            }
        }
    }
}
