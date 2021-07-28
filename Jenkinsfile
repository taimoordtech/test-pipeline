pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
            git pull origin main
            '''
            }
        }
        stage('Test') {
            steps {
                echo 'Baby please...'
            }
        }
    }
}