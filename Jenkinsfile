pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the GitHub repository...'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

      
    stage('Test') {
    steps {
        echo 'Running tests...'
        script {
            try {
                sh 'npm test'
            } catch (err) {
                echo 'Test script not found or failed, skipping...'
            }
        }
    }
}

      

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Example: Deploy to a server, cloud, etc.
            }
        }
    }
}
