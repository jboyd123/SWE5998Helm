pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/kubernetes/ingress-nginx.git'
            }
        }
        stage('Deploy Helm chart') {
            steps {
                sh "helm install ingress-nginx ./deploy/charts/ingress-nginx --namespace ingress-nginx --set controller.publishService.enabled=true --set controller.service.loadBalancerIP=${env.LB_IP}"
            }
        }
    }
}