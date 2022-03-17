pipeline {
    agent any
    tools {
        terraform 'terraform-11'
    }

    stages {
        stage('Git SCM Checkout') {
            steps {
                git credentialsId: '6c778052-91d3-47f4-9be6-c74b05b3adde', url: 'https://github.com/KrishnaPal-TTN/TTN-WorkShop.git'
            }
        }
        stage('Terraform init') {
            steps {
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
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
