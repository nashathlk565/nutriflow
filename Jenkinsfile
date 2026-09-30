pipeline {
    agent any

    stages {

        stage('Check Files') {
            steps {
                bat 'dir /s /b'
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('frontend') {
                    bat 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                dir('frontend') {
                    bat 'npm run build'
                }
            }
        }
    }
}