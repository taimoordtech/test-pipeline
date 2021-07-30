pipeline {

    agent {
        node {
            label 'master'
        }
    }

    options {
        buildDiscarder logRotator( 
                    daysToKeepStr: '16', 
                    numToKeepStr: '10'
            )
    }

    stages {

         stage("Build") {
            steps {
                 sh 'php --version'
                sh 'composer install'
                sh 'composer --version'
                sh 'cp .env.example .env'
                sh 'php artisan key:generate'
            }
        }
        
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
                sh """
                echo "Cleaned Up Workspace For Project"
                """
            }
        }



        stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/taimoordtech/test-pipeline.git']]
                ])
            }
        }

       

        stage(' Unit Testing') {
             steps {
                sh 'php artisan test'
            }
        }

         stage("Code coverage") {
            steps {
                sh "vendor/bin/phpunit --coverage-html 'reports/coverage'"
            }
        }

        stage('Code Analysis') {
            steps {
                sh """
                echo "Running Code Analysis"
                """
            }
        }

        stage('Build Deploy Code') {
            when {
                branch 'main'
            }
            steps {
                sh """
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
        }

    }   
}