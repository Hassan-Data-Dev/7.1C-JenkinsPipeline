pipeline {
    agent any

    stages {
        stage('Stage 1: Build') {
            steps {
                echo 'Task: Compile and package the code.'
                echo 'Tool: Maven'
            }
        }
        stage('Stage 2: Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests (code correctness) and integration tests (component interactions).'
                echo 'Tool: JUnit + Testcontainers'
            }
        }
        stage('Stage 3: Static Code Analysis') {
            steps {
                echo 'Task: Detect bugs, code smells and maintainability issues.'
                echo 'Tool: SonarQube / SonarCloud'
            }
        }
        stage('Stage 4: Dependency Security Scan') {
            steps {
                echo 'Task: Scan libraries/dependencies for known vulnerabilities (DevSecOps).'
                echo 'Tool: OWASP Dependency-Check / Snyk'
            }
        }
        stage('Stage 5: Package Artifact') {
            steps {
                echo 'Task: Package the validated code into a deployable artifact.'
                echo 'Tool: Maven package / Docker build'
            }
        }
        stage('Stage 6: Deploy to Staging') {
            steps {
                echo 'Task: Deploy the artifact to a staging environment.'
                echo 'Tool: Ansible / Docker Compose'
            }
        }
        stage('Stage 7: Report and Notify') {
            steps {
                echo 'Task: Report build outcome and notify the team.'
                echo 'Tool: Extended Email Notification / Slack'
            }
        }
    }

    post {
        always   { echo "Pipeline finished. Result: ${currentBuild.currentResult}" }
        success  { echo 'Build SUCCESS' }
        failure  { echo 'Build FAILED' }
    }
}