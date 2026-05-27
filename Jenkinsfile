pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')
    }

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-website .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker rm -f devops-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh '''
                docker run -d \
                --name devops-container \
                -p 80:80 \
                devops-website
                '''
            }
        }
    }
}