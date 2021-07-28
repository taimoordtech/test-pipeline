pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
                cd /var/www/html/test-pipeline/
                git pull origin main
            '''
            }
        }
        stage('Test') {
            steps {
                echo 'testing'
            }
        }
    }
}