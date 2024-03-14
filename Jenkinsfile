pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests'
                echo 'Running integration tests'
            } 
post{
success{
mail to: 'Vkingk2@gmail.com',
subject: 'Unit and integration test running',
body: 'Unit and integration test successfully passed'
}
failure{
mail to: 'Vkingk2@gmail.com',
subject: 'Unit and integration test run failed',
body: 'Unit and integration test failed'
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
                echo 'Performing security scan'
            }
post{
success{
mail to: 'Vkingk2@gmail.com',
subject: 'Security test running',
body: 'Security test successfully passed'
}
failure{
mail to: 'Vkingk2@gmail.com',
subject: 'Security test run failed',
body: 'Security test failed'
}

}
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to staging server'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to production server'
            }
        }
    }
}
