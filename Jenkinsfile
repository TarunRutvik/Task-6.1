pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building ..."
                // Add your build automation tool here, e.g., Maven
            }
            post{
                always{
                    mail to: "gandeti.tarun@gmail.com",
                    subject: "Build Status Email",
                    body: "Build log attached!"
                }
            }
        }
        stage("Unit and Integration Tests"){
            steps{
                echo "Running Unit and Integration Tests ..."
                // Specify your test automation tool, e.g., JUnit
            }
        }
        stage("Code Analysis"){
            steps{
                echo "Performing Code Analysis ..."
                // Add code analysis tool, e.g., SonarQube
            }
        }
        stage("Security Scan"){
            steps{
                echo "Performing Security Scan ..."
                // Add security scan tool, e.g., OWASP Dependency Check
            }
        }
        stage("Deploy to Staging"){
            steps{
                echo "Deploying to Staging ..."
                // Add steps to deploy to staging server, e.g., AWS EC2
            }
        }
        stage("Integration Tests on Staging"){
            steps{
                echo "Running Integration Tests on Staging ..."
            }
        }
        stage("Deploy to Production"){
            steps{
                echo "Deploying to Production ..."
                // Add steps to deploy to production server, e.g., AWS EC2
            }
        }
        stage("Complete"){
            steps{
                echo "Completed"
            }
     }
    }
}