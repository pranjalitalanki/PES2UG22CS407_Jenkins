pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    echo "Compiling the C++ file..."
                    g++ -o YOUR_SRN-1 main.cpp
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh '''
                    echo "Running the C++ program..."
                    ./YOUR_SRN-1
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
