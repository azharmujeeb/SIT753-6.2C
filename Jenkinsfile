pipeline {
    agent any // This specifies that the pipeline can run on any available agent (Jenkins slave).
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install' // Example Maven build command
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test' // Example Maven test command
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
