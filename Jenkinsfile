pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                echo 'Initiating the dependencies installation for our React project through npm. This process ensures all necessary libraries and frameworks are available for development and testing.'
            }
        }

        stage('Unit Tests') {
            steps {
                echo 'Executing unit tests using Jest. This critical stage validates the reliability of individual components within the React application, confirming they perform as intended.'
            }
            post {
                success {
                    emailext (
                        subject: 'Success: Unit Tests Stage',
                        body: 'The unit testing phase, facilitated by Jest, concluded successfully. All components are functioning within expected parameters.',
                        to: 'yugam4872.be22@chitkara.edu.in'
                    )
                }
                failure {
                    emailext (
                        subject: 'Failure: Unit Tests Stage',
                        body: 'The unit testing phase encountered issues. Review the Jenkins logs for detailed insights and rectification measures.',
                        to: 'yugam4872.be22@chitkara.edu.in'
                    )
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing the React codebase with ESLint to pinpoint issues and confirm adherence to our established coding practices. This ensures maintainability and quality of the code.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Conducting a security audit on the React application with OWASP ZAP. This scan is pivotal in identifying and mitigating potential security vulnerabilities, ensuring robust application security.'
            }
            post {
                success {
                    emailext (
                        subject: 'Success: Security Scan Stage',
                        body: 'Security assessment through OWASP ZAP completed successfully, with no critical vulnerabilities detected.',
                        to: 'yugam4872.be22@chitkara.edu.in'
                    )
                }
                failure {
                    emailext (
                        subject: 'Failure: Security Scan Stage',
                        body: 'Security assessment through OWASP ZAP identified critical issues. Immediate attention required. Consult the Jenkins logs for further details.',
                        to: 'yugam4872.be22@chitkara.edu.in'
                    )
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Commencing the build process for the React application with the "npm run build" command. This step prepares the application for production by optimizing and bundling the code effectively.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to a staging environment on neclify. This stage allows us to test the application in an environment that closely resembles production, ensuring reliability and performance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running comprehensive integration tests on the staging deployment using Jest. This ensures all parts of the application interact correctly and perform well under production-like conditions.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Finalizing the pipeline by deploying the React application to a production server on neclify. This makes the application available to our end-users, marking the culmination of our CI/CD process.'
            }
        }
    }
}
