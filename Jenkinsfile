pipeline {
    agent any

    stages {
        stage('Coding') {
            steps {
                echo 'Preparing Python application'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t tutorial-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker rm -f tutorial-app || true'
                sh 'docker run -d --name tutorial-app tutorial-app tail -f /dev/null'
            }
        }

        stage('Verify Deployment') {
            steps {
                sh 'docker exec tutorial-app python3 app.py'
            }
        }
    }
}
