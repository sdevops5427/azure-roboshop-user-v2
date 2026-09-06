pipeline {

    agent any

    stages {
        stage('CheckOut') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sdevops5427/roboshop-user-v1.git'
            }
        }
        stage('Build Image') {
            steps {
                sh "docker build -t user ."
            }
        }
        stage('Tag Image') {
            steps {
                sh "docker tag cart roboshop0088.azurecr.io/user:latest"
            }
        }
        stage('Push Image') {
            steps {
                sh "docker push roboshop0088.azurecr.io/user"
            }
        }
    }
}
