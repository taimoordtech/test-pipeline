pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh '''
            git pull origin main
            '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
    }
}