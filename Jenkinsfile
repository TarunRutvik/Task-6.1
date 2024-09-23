pipeline{
    agent any
     stages {
        stage('Build') {
            steps {
                script {
                    echo "Fetching the source code",
                    echo "Compile the code and generate any necessary artifacts"
                }
            }
        }

        stage('Test') {
            steps {
                echo "Running unit tests",
                echo "Running integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('Approval') {
            steps {
                echo "Simulating manual approval...",
                sleep time: 10, unit: 'SECONDS'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to the production environment"
            }
       }
    }
post {
        success {
            mail to: "gandeti.tarun@gmail.com",
            subject: "Build Successful",
            body: "The build has completed successfully. "
        }
        failure {
            mail to: "gandeti.tarun@gmail.com",
            subject: "Build Failed",
            body: "The build has failed. Please check the logs.",
       }
     }

}