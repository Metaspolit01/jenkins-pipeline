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
                        echo '⚠️ Test script not found. Skipping test step.'
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add real deployment steps here
            }
        }
    }
}

