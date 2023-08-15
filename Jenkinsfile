pipeline {
    agent any

    stages {
        stage('Namespaces') {
            steps {
                script {
                    withKubeConfig([credentialsId: EKS_CREDENTIALS, serverUrl: EKS_SERVER_URL]) {
                        sh 'kubectl apply -f namespaces.yaml'
                    }
                }
            }
        }
    }
}
