pipeline {
    agent any
    
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Build the code using a build automation tool (e.g., Maven)
                // Example:
                // sh 'mvn clean package'
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                // Run unit tests and integration tests
                // Example:
                // sh 'mvn test'
            }
        }
        
        stage('Code Analysis') {
            steps {
                // Integrate a code analysis tool to analyze the code
                // Example:
                // sh 'sonar-scanner'
            }
        }
        
        stage('Security Scan') {
            steps {
                // Perform a security scan on the code
                // Example:
                // sh 'npm audit'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                // Deploy the application to a staging server
                // Example:
                // sh 'ansible-playbook deploy_staging.yml'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on the staging environment
                // Example:
                // sh 'robot -d results tests/'
            }
        }
        
        stage('Deploy to Production') {
            steps {
                // Deploy the application to a production server
                // Example:
                // sh 'ansible-playbook deploy_production.yml'
            }
        }
    }
    
    post {
                success {
                    emailext subject: 'Build Successful',
                        body: 'Build completed successfully',
                        to: 'gpranav2901@gmail.com'
                }
                failure {
                    emailext subject: 'Build Failed',
                        body: 'Build failed',
                        to: 'gpranav2901@gmail.com'
                }
        }
    }

