pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/gurubasavaraj7/Devops-July2025.git'
            }
        }
        stage('BUILD') {
            steps {
                sh '''
                    ls -lrt
                    pwd
                '''
            }
        }
        stage {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/gurubasavaraj7/Jenkins-july25.git']])
            }
        }
        
        stage('BUILD2') {
            steps {
                sh '''
                    ls -lrt
                    pwd
                '''
            }
        }
    }
}