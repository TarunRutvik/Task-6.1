pipeline {
    agent any

    environment {
        EMAIL_RECIPIENT = 'dev-team@example.com'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code from GitHub...'
                git 'https://github.com/your-username/simple-python-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // For Python, we don't have a build step, but we can just echo.
                echo 'Build step completed (no artifacts to build).'
            }
        }

        stage('Unit Tests') {
            steps {
                echo 'Running unit tests...'
                sh 'python -m unittest discover -s test'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
                // Example for staging deployment
                sh 'echo "Deploying to staging server..."'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                // Placeholder for integration tests
                echo 'Integration tests completed.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
                sh 'echo "Deploying to production server..."'
            }
        }
    }

    post {
        success {
            mail to: "${gandeti.tarun@gmail.com}",
                 subject: "Build Successful: ",
                 body: "The build has completed successfully.",
        }
        failure {
            mail to: "${gandeti.tarun@gmail.com}",
                 subject: "Build Failed: ",
                 body: "The build has failed. Please check the logs.",
                 attachLog: true
      }
    }
}