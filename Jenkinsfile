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
    }
}