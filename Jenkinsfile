pipeline {
    agent any

    stages {
        stage('Stage 1: Build') {
            steps {
                echo 'Initiating build process...'
                echo 'Compiling and packaging the React application...'
                echo 'Tool used: Webpack or Vite'
            }
        }

        stage('Stage 2: Unit and Integration Tests') {
            steps {
                echo 'Executing unit and integration tests...'
                echo 'Ensuring React components and functionality perform as expected...'
                echo 'Tools used: Jest, Cypress, or Selenium'
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

        stage('Stage 3: Code Analysis') {
            steps {
                echo 'Conducting code analysis...'
                echo 'Analyzing the React code to ensure adherence to industry standards...'
                echo 'Tools used: ESLint or SonarQube'
            }
        }

        stage('Stage 4: Security Scan') {
            steps {
                echo 'Performing security scan...'
                echo 'Identifying potential vulnerabilities within the React application...'
                echo 'Tools used: OWASP ZAP or other security scanners'
            }
            post {
                success {
                    emailext attachLog: true, body: "Stage 4: Security Scan passed successfully.", subject: "Pipeline Notification: Stage 4 Passed", to: "vkingk2@gmail.com"
                }
                failure {
                    emailext attachLog: true, body: "Stage 4: Security Scan failed. Please review the logs for details.", subject: "Pipeline Notification: Stage 4 Failed", to: "vkingk2@gmail.com"
                }
            }
        }

        stage('Stage 5: Deploy to Staging') {
            steps {
                echo 'Deploying React application to staging environment...'
                echo 'Preparing for testing and preview...'
                echo 'Tools used: AWS S3 or Netlify'
            }
        }

        stage('Stage 6: Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment...'
                echo 'Ensuring application functions correctly in a production-like environment...'
                echo 'Tools used: Cypress or Selenium'
            }
        }

        stage('Stage 7: Deploy to Production') {
            steps {
                echo 'Deploying React application to production environment...'
                echo 'Finalizing deployment for live usage...'
                echo 'Tools used: AWS S3, Netlify, or a web server'
            }
        }
    }
}
