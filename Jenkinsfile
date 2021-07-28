pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
                cd /var/www/html/test-pipeline/
                chown -R root:www-data .git
                git pull origin main
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Baby please na...'
            }
        }
    }
}