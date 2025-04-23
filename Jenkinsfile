pipeline{
    agent any
    stages {
    
        stage('Setup Python Virtual ENV for dependencies'){
            steps  {
                sh '''
                sh 'chmod +x scripts/envsetup.sh'
                ./scripts/envsetup.sh
                '''
            }
        }
        stage('Setup Gunicorn Setup'){
            steps {
                sh '''
                chmod +x scripts/gunicorn.sh
                ./gunicorn.sh
                '''
            }
        }
        stage('setup NGINX'){
            steps {
                sh '''
                chmod +x scripts/nginx.sh
                ./nginx.sh
                '''
            }
        }
    }
}
