pipeline {
    agent any

    stages {
        stage('Stage 1: Build') {
            steps {
                echo 'Task: Build the code using a build automation tool to compile and package your code.'
                echo 'Tool: Maven'
            }
        }
        stage('Stage 2: Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected.'
                echo 'Tool: JUnit (unit tests) / Selenium (integration tests)'
            }
        }
        stage('Stage 3: Code Analysis') {
            steps {
                echo 'Task: Analyse the code using a code analysis tool to ensure it meets industry standards.'
                echo 'Tool: SonarQube'
            }
        }
        stage('Stage 4: Security Scan') {
            steps {
                echo 'Task: Perform a security scan on the code to identify any vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }
        stage('Stage 5: Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging server.'
                echo 'Tool: AWS EC2 instance (via SSH/SCP)'
            }
        }
        stage('Stage 6: Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests on the staging environment to ensure the application functions as expected in a production-like environment.'
                echo 'Tool: Selenium'
            }
        }
        stage('Stage 7: Deploy to Production') {
            steps {
                echo 'Task: Deploy the application to a production server.'
                echo 'Tool: AWS EC2 instance (via SSH/SCP)'
            }
        }
    }

    post {
        always   { echo "Pipeline finished. Result: ${currentBuild.currentResult}" }
        success  { echo 'Build SUCCESS' }
        failure  { echo 'Build FAILED' }
    }
}