pipeline {
    agent any

    environment {
        AWS_DEFAULT_REGION = 'ap-south-1'  // Replace with your region
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/your-repo/terraform-ecs.git'  // Replace with your repo URL
                sh 'ls -la'  // Check that the files are present
            }
        }
        stage('Terraform Init') {
            steps {
                dir('terraform-ecs') {  // Replace with the correct subdirectory if needed
                    sh 'terraform init'
                }
            }
        }
        stage('Terraform Plan') {
            steps {
                dir('terraform-ecs') {  // Replace with the correct subdirectory if needed
                    sh 'terraform plan'
                }
            }
        }
        stage('Terraform Apply') {
            steps {
                dir('terraform-ecs') {  // Replace with the correct subdirectory if needed
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
