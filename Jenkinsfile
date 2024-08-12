pipeline {
    agent any

    environment {
        AWS_DEFAULT_REGION = 'ap-south-a'  // Replace with your region
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/agarwalpoonam01/accelon-assignment.git'  // Replace with your repo URL
            }
        }
        stage('Terraform Init') {
            steps {
                sh 'cd accelon-assignment'
                sh 'terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}

