pipeline {
    agent any  // Use any available agent or node

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the public GitHub repository
                git url: 'https://github.com/sukahermawan/Lab.git'
            }
        }

        stage('Build') {
            steps {
                // Run the Maven build command
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run the Maven test command
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Placeholder for deployment steps
                bat 'echo "Deploying application..."'
            }
        }
    }

    post {
        always {
            // Actions that will always be executed
            echo 'This will always run after the stages'
        }

        success {
            // Actions if the build succeeds
            echo 'Build succeeded!'
        }

        failure {
            // Actions if the build fails
            echo 'Build failed.'
        }
    }
}
