pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'  // Compile C++ file
            }
        }
        stage('Test') {
            steps {
                sh './output'  // Execute compiled C++ file
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
