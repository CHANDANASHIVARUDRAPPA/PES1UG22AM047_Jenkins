pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o YOUR_SRN-1 main.cpp'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './YOUR_SRN-1'  // Run the compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
