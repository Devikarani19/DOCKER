pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:alpine').inside {
                        // Place your commands here, like:
                        sh 'npm install'
                        sh 'npm run build'
                    }
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-node-app', '.')
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    docker.image('my-node-app').inside {
                        sh 'npm test'
                    }
                }
            }
        }
    }
}
    
