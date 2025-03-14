pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o output main.cpp'  // Replace 'main.cpp' with your actual source file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh './output'  // Execute compiled output file (assuming it runs tests)
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'scp output user@yourserver:/path/to/deploy/'  // Modify with actual server details
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
