pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git credentialsId: 'ddf31db6-be59-4319-a43c-9b6e6a7306ad', url: 'https://github.com/shrinand12B/Seleniumtest'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running automation tests...'
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
