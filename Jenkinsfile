pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh "echo 'Starting build...'"
                }
            }
        }

        stage('Test') {
            steps {
                sh "echo './run-tests.sh'"
            }
        }

        stage('Deploy') {
            steps {
                sh "echo './deploy.sh'"
            }
        }
    }
}
