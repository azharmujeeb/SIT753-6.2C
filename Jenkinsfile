pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building' // Replace with your build commands
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and Integration Tests' // Replace with your test commands
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'// Integrate a code analysis tool (e.g., SonarQube) here
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Security Scan'// Integrate a security scanning tool (e.g., OWASP ZAP) here
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging'// Deploy to a staging environment (e.g., AWS EC2) here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging'// Run integration tests on the staging environment here
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production'// Deploy to a production environment (e.g., AWS EC2) here
            }
        }
    }
    post {
        success {
            emailext(
                subject: "Pipeline Successful",
                body: "The Jenkins pipeline completed successfully.",
                to: 'ja.mujeeb.06@gmail.com',
            )
        }
        failure {
            emailext(
                subject: "Pipeline Failed",
                body: "The Jenkins pipeline failed. Please check the logs for details.",
                to: 'ja.mujeeb.06@gmail.com',
            )
        }
    }
}
