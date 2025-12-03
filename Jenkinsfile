pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                echo "Pulling code from GitHub..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build stage (not needed for HTML)."
            }
        }

        stage('Test') {
            steps {
                echo "Running basic tests..."
                sh "grep -i 'hello' index.html"   // simple test
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to /var/www/html"
                sh "sudo cp -r * /var/www/html/"
            }
        }
    }
}
