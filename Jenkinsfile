pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the C++ program...'
                make -C main
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the C++ program...'
                sh './main/hello_exec'
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
