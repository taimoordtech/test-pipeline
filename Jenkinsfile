pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git pull origin main
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
    }
}