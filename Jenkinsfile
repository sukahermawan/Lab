pipeline {
    agent any  // Use any available agent or node

    //environment {
        // Define any environment variables you need here
        // For example, JAVA_HOME for Java projects
        // JAVA_HOME = 'C:\\Program Files\\Java\\jdk-11'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the public GitHub repository
                git url: 'https://github.com/sukahermawan/Lab.git'
            }
        }

        stage('Build') {
            steps {
                // Example for a Maven build
                // Adjust this step according to your project's build tool (e.g., Gradle, Ant, etc.)
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Example for running tests
                // Adjust this step according to your project's testing framework
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Example for deployment
                // Adjust this step according to your deployment process
                bat 'echo "Deploying application..."'
                // You can add deployment scripts or commands here
            }
        }
    }

    post {
        always {
            // Actions that will always be executed, such as cleanup
            echo 'This will always run after the stages'
        }

        success {
            // Actions that will be executed if the build succeeds
            echo 'Build succeeded!'
        }

        failure {
            // Actions that will be executed if the build fails
            echo 'Build failed.'
        }
    }

