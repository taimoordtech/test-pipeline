pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
                cd /var/www/html/test-pipeline/
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