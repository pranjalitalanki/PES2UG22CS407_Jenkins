pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    echo "Compiling the C++ file..."
                    g++ -o PES2UG22CS407_1 main.cpp
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh '''
                    echo "Running the C++ program..."
                    ./PES2UG22CS407_1
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
                // Add deployment commands here
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
