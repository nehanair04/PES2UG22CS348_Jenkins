pipeline {
    agent any  // Runs pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new.cpp -o PES2UG22CS348' // Compile hello.cpp and generate PES2UG22CS348 executable
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS348' // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
