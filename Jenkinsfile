pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using Maven'
            }
            post {
                success {
                   emailext attachLog: true,  body: "Build successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Run unit tests using JUnit'
                echo 'Run integration tests using Selenium'
            }
            post {
                success {
                    emailext attachLog: true, body: "Unit and Integration Tests successful", subject: "Build succeeded", to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Integrate SonarQube to analyse the code'
            }
            post {
                success {
                    emailext attachLog: true, body: "Code Analysis successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Perform security scan using OWASP ZAP'
            }
            post {
                success {
                    emailext attachLog: true, body: "Security Scan successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy the application to AWS EC2 instance'
            }
            post {
                success {
                    emailext attachLog: true, body: "Deploy to Staging successful", subject: "Build succeeded", to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Run integration tests on the staging environment using Selenium'
            }
            post {
                success {
                    emailext attachLog: true, body: "Integration Tests on Staging successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to AWS EC2 instance'
            }
            post {
                success {
                    emailext attachLog: true, body: "Deploy to Production successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
    }

    post {
                success {
                    emailext attachLog: true, body: "overall Build was successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    emailext attachLog: true, body: "overall Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
}

