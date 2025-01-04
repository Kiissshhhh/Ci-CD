pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t product-service .'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f product-deployment.yaml'
            }
        }
    }
}
