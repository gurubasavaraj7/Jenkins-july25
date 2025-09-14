pipeline { 
    agent any

    stages {
        stage('Checkout'){
            steps {
            git branch: 'main', credentialsId: 'github', url: 'https://github.com/gurubasavaraj7/Devops-July2025.git'
        }
    }
        stage('Parallel steps') {
            parallel {
                stage('Checkout Code quality') {
                    steps {
                        sh '''
                            ls -lrt
                            pwd
                        '''
                    }
                }
                           

                stage('BUILD'){
                    steps {
                        sh '''
                            echo "Build started"
                            ls -lrt
                            sudo appt update -y
                            sudo apt install maven -y
                            mvn clean install   
                            echo "Build completed"  
                        '''  
                    }
                }    
                                           
            }
                
        }
    }    
}