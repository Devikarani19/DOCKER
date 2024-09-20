pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
               'https://github.com/Devikarani19/DOCKER.git'
            }
        }
    
        stage('Make Changes') {
            steps {
                script {
                    sh 'echo " one more info" >> README.md'
                }
            }
        }
        stage('git init') {
            steps {
                sh 'git init'
            }
        }
        stage('git add') {
            steps {
                sh 'git add .'
            }
        }

        stage('git commit') {
            steps {
                sh 'git commit -m "updates"'
            }
        }
    }
}


     
