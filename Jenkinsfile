pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
                cd /var/www/html/test-pipeline/
            git pull
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