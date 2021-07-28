pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
            sudo git pull origin main
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