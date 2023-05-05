pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using Maven'
            }
            post {
                success {
                    archiveArtifacts 'build.log'
                    mail body: "Build successful", subject: "Build succeeded", attachmentPattern: 'build.log',  to: '3444gauravsharma@gmail.com'
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
                    mail body: "Unit and Integration Tests successful", subject: "Build succeeded", to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Integrate SonarQube to analyse the code'
            }
            post {
                success {
                    mail body: "Code Analysis successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Perform security scan using OWASP ZAP'
            }
            post {
                success {
                    mail body: "Security Scan successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy the application to AWS EC2 instance'
            }
            post {
                success {
                    mail body: "Deploy to Staging successful", subject: "Build succeeded", to: 'youremail@example.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: 'youremail@example.com'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Run integration tests on the staging environment using Selenium'
            }
            post {
                success {
                    mail body: "Integration Tests on Staging successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to AWS EC2 instance'
            }
            post {
                success {
                    mail body: "Deploy to Production successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
        }
    }

    post {
                success {
                    mail body: "overall Build was successful", subject: "Build succeeded",  to: '3444gauravsharma@gmail.com'
                }
                failure {
                    mail body: "overall Build failed", subject: "Build failed",  to: '3444gauravsharma@gmail.com'
                }
            }
}