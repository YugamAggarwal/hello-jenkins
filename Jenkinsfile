pipeline {
    agent any

    stages {
        stage('Stage 1: Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Compile and package the React application using a bundler like Webpack or Vite.'
                echo 'Tool used: Webpack or Vite'
            }
        }

        stage('Stage 2: Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Run unit tests using Jest or other testing frameworks to ensure the React components and functionality work as expected. Additionally, run integration tests using tools like Cypress or Selenium to test the application as a whole.'
                echo 'Tools used: Jest, Cypress, or Selenium'
            }
            post {
                success {
                    emailext attachLog: true, body: "Stage 2: Unit and Integration Tests passed successfully.", subject: "Pipeline Notification: Stage 2 Passed", to: "yugam4872.be22@chitkara.edu.in"
                }
                failure {
                    emailext attachLog: true, body: "Stage 2: Unit and Integration Tests failed. Please check the logs for details.", subject: "Pipeline Notification: Stage 2 Failed", to: "yugam4872.be22@chitkara.edu.in"
                }
            }
        }

        stage('Stage 3: Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Integrate code analysis tools like ESLint or SonarQube to analyze the React code and ensure it meets industry standards and best practices.'
                echo 'Tool used: ESLint or SonarQube'
            }
        }

        stage('Stage 4: Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Perform a security scan on the React application using tools like OWASP ZAP or other security scanners to identify potential vulnerabilities.'
                echo 'Tool used: OWASP ZAP or other security scanners'
            }
            post {
                success {
                    emailext attachLog: true, body: "Stage 4: Security Scan passed successfully.", subject: "Pipeline Notification: Stage 4 Passed", to: "yugam4872.be22@chitkara.edu.in"
                }
                failure {
                    emailext attachLog: true, body: "Stage 4: Security Scan failed. Please check the logs for details.", subject: "Pipeline Notification: Stage 4 Failed", to: "yugam4872.be22@chitkara.edu.in"
                }
            }
        }

        stage('Stage 5: Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Deploy the React application to a staging environment (e.g., AWS S3 bucket or Netlify) for testing and preview.'
                echo 'Tool used: AWS S3 or Netlify'
            }
        }

        stage('Stage 6: Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Run integration tests on the staged React application using tools like Cypress or Selenium to ensure it functions as expected in a production-like environment.'
                echo 'Tool used: Cypress or Selenium'
            }
        }

        stage('Stage 7: Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Deploy the React application to the production environment (e.g., AWS S3 bucket, Netlify, or a web server).'
                echo 'Tool used: AWS S3, Netlify, or a web server'
            }
        }
    }
}
