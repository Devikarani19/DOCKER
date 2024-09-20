pipeline {
    agent any

    environment {
        IMAGE_NAME = 'nodejs' // Change this to your desired image name
        CONTAINER_NAME = 'devika' // Name for your running container
    }

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git url: 'https://github.com/Devikarani19/DOCKER.git', branch: 'main' // Adjust branch as needed
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Build the Docker image using the Dockerfile in the repo
                    docker.build("${nodejs}", ".")
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Run tests inside the Docker container
                    docker.image("${nodejs}").inside {
                        sh 'npm install' // Install dependencies
                        sh 'npm test'    // Run tests
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Stop and remove the existing container if it exists
                    sh "docker stop ${devika} || true"
                    sh "docker rm ${devika} || true"

                    // Run the container
                    docker.image("${nodejs}").run("-d --name ${devika} -p 3000:3000") // Adjust ports as needed
                }
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed!'
        }
    }
}
