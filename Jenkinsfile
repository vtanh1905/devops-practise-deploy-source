pipeline {
    agent any

    stages {
        stage('Namespaces') {
            steps {
                sh 'kubectl apply -f namespaces.yaml'
            }
        }

        stage('Deployment') {
            steps {
                sh 'kubectl apply -f deployments.yaml'
            }
        }

        stage('Services') {
            steps {
                sh 'kubectl apply -f services.yaml'
            }
        }
    }
}
