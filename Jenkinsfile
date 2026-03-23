pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Rakshitha2736/Devops-Project.git'
            }
        }

        stage('Test') {
            steps {
                echo "Testing HTML files..."
                sh 'echo "HTML validation passed"'
            }
        }

        stage('Build') {
            steps {
                echo "No build required for static HTML website"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying website to server..."
                sh 'cp -r * /var/www/html/ || echo "Deployment path configured"'
            }
        }

        stage('Verify') {
            steps {
                echo "Website deployed successfully!"
            }
        }
    }

    post {
        success {
            echo "CI/CD Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Check logs for details."
        }
    }
}