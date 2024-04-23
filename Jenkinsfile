pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Build the code using Maven."
                // Tool: Maven
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Run unit and integration tests using JUnit and Selenium."
                // Tools: JUnit, Selenium
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Analyse code using SonarQube."
                // Tool: SonarQube
            }
        }
        stage('Security Scan') {
            steps {
                echo "Perform security scan using OWASP ZAP."
                // Tool: OWASP ZAP
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploy to AWS EC2 staging instance."
                // Tool: AWS EC2, Jenkins Deploy plugin
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Run integration tests in staging."
                // Tools: Selenium, Postman
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy to AWS EC2 production instance."
                // Tool: AWS EC2, Jenkins Deploy plugin
            }
        }
    }
    post {
        always {
            mail to: 'your-email@example.com',
                 subject: "Stage Completed: ${currentBuild.fullDisplayName}",
                 body: "Check console output at ${env.BUILD_URL} to view the results.",
                 attachLog: true
        }
    }
}