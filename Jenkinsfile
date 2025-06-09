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
                sh'''
                    docker --version
                    docker-compose --version
                    docker-compose down -v --rmi all --remove-orphans 
                    # docker ps --format '{{.ID}} {{.Names}} {{.Ports}}' | grep 2375


                     docker-compose up -d'''
            }
        }
}
}