pipeline {
    agent any // Specifies the agent to run the pipeline

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/sukahermawan/Lab', branch: 'master'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
