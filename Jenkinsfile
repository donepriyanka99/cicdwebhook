pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Code Cloned Successfully'
            }
        }

        stage('Build') {
            steps {
                echo 'Installing Dependencies'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Application'
                sh 'nohup node app.js > output.log 2>&1 &'
                sh 'sleep 5'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Application Deployed Successfully'
            }
        }
    }

    post {

        success {
            echo 'Pipeline Success'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}
