pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    buildCmd = "nohup ./your-build-script.sh &"
                    sh "echo 'Starting build...'"
                    sh buildCmd
                }
            }
        }

        stage('Test') {
            steps {
                sh './run-tests.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh './deploy.sh'
            }
        }
    }
}
