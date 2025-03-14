pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make'  // Use Makefile to compile
            }
        }
        stage('Test') {
            steps {
                sh './output'  // Run the compiled executable
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
