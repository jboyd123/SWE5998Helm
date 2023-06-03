pipeline {
    agent any
    stages {
        stage('Deploy Helm chart') {
            steps {
                bat "helm repo add cloudecho https://cloudecho.github.io/charts/; helm repo update; helm install my-hello cloudecho/hello -n default --version=0.1.2"
            }
        }
    }
}