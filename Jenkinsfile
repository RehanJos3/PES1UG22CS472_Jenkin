pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ hello.cpp -o hello_exec'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './non_existing_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment stage (simulated)"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed!"
        }
    }
}
