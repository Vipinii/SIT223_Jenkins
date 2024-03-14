pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Compiling the code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Executing unit tests'
                echo 'Conducting integration tests'
            }
            post {
                success {
                    mail to: 'vkingk2@gmail.com',
                    subject: 'Unit and integration test execution in progress',
                    body: 'Unit and integration tests have been successfully executed'
                }
                failure {
                    mail to: 'vkingk2@gmail.com',
                    subject: 'Failure in unit and integration test execution',
                    body: 'Unit and integration tests have failed'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Conducting security scan'
            }
            post {
                success {
                    mail to: 'vkingk2@gmail.com',
                    subject: 'Security scan in progress',
                    body: 'Security scan has been successfully completed'
                }
                failure {
                    mail to: 'vkingk2@gmail.com',
                    subject: 'Failure in security scan',
                    body: 'Security scan has failed'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to staging environment'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging server'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to production server'
            }
        }
    }
}
