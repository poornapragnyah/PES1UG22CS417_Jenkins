pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the C++ program...'
                sh 'g++ -o PES1UG22CS417-1 hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the C++ program...'
                sh './PES1UG22CS417-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the build...'
                echo 'Deployment step can be customized as needed.'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed.'
        }
        success {
            echo 'Pipeline completed successfully.'
        }
    }
}
