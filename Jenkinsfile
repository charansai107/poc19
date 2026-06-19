pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Deploy') {
            steps {
                sh 'ansible-playbook deploy.yml'
            }
        }

    }

    post {
        success {
            echo 'Application deployed successfully.'
        }

        failure {
            echo 'Deployment failed.'
        }
    }
}
