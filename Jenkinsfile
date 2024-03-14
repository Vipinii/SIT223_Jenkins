pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo "Stage: Build"
                    echo "Description: Build the code using Maven"
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo "Stage: Unit and Integration Tests"
                    echo "Description: Run unit tests and integration tests"
                }
            }
            post {
                success {
                    emailext attachLog: true, body: "Stage 2: Tests passed successfully.", subject: "Pipeline Notification: Stage 2 Passed", to: "vkingk2@gmail.com"
                }
                failure {
                    emailext attachLog: true, body: "Stage 2: Tests failed. Please review the logs for details.", subject: "Pipeline Notification: Stage 2 Failed", to: "vkingk2@gmail.com"
                }
            }
        }

        }

        stage('Code Analysis') {
            steps {
                script {
                    echo "Stage: Code Analysis"
                    echo "Description: Analyze code quality using SonarQube"
                }
            }
        }

        stage('Security Scan') {
            steps {
                script {
                    echo "Stage: Security Scan"
                    echo "Description: Perform security scan using OWASP Dependency-Check"
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                script {
                    echo "Stage: Deploy to Staging"
                    echo "Description: Deploy the application to staging server: ${env.STAGING_SERVER}"
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo "Stage: Integration Tests on Staging"
                    echo "Description: Run integration tests on staging environment"
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    echo "Stage: Deploy to Production"
                    echo "Description: Deploy the application to production server: ${env.PRODUCTION_SERVER}"
                }
            }
        }
    }
}
