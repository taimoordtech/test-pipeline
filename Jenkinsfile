pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Deploying...'
                sh '''
                cd /var/www/html/test-pipeline/
                chmod g+w .git -R
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