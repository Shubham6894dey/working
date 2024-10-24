pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository
                git 'https://github.com/Shubham6894dey/working'
            }
        }

        stage('Build') {
            steps {
                // Compile the Java program
                bat 'javac App.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                bat 'java App'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Build the Docker image
                script {
                    docker.build('demo-java-project')
                }
            }
        }
        

        
    }
}
