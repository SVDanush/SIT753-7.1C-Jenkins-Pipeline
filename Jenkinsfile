pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Build: Compile and package the code using Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and Integration Tests: Run unit tests using JUnit and integration tests using Selenium.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis: Analyse code quality and coding standards using SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security Scan: Scan the code for known vulnerabilities using OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging: Deploy the application to an AWS EC2 staging environment.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging: Run integration tests against the staging environment.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production: Deploy the application to an AWS EC2 production environment.'
            }
        }
    }
}
