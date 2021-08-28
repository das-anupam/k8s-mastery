pipeline {
    stages {
        stage('Build sa-frontend') {
            steps {
                sh 'cd sa-frontend && npm install && npm run build'
            }
        }
        stage('Build sa-webapp') {
            steps {
                sh 'cd sa-webapp && mvn install'
            }
        }
        stage('Docker image Building for sa-frontend') {
            steps {
                sh 'cd sa-frontend && docker build -t sa-frontend .'
            }
        }
        stage('Docker image Building for sa-webapp') {
            steps {
                sh 'cd sa-webapp && docker build -t sa-webapp .'
            }
        }
    }
}