pipeline {
    agent any  // Runs pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new_hello.cpp -o PES2UG22CS347' // Compile new_hello.cpp and generate PES2UG22CS347 executable
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './WRONG_EXECUTABLE' // Intentional error: Wrong executable name
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'  // Simulated deployment step
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Display failure message if any stage fails
        }
    }
}
