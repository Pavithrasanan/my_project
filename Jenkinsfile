pipeline{
    agent any
    stages{
        stage('Backed'){
            steps{
                sh'docker build -t chat-backend ./backend'
            }
        }
        stage('Frontend'){
            steps{
                sh'docker build -t chat-frontend ./frontend'
            }
        }
        stage('Deploy'){
            steps{
                sh'docker compose up -d'
            }
        }
}
}