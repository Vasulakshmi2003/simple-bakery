pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git branch: 'main', url: 'https://github.com/Vasulakshmi2003/simple-bakery.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build your project (example with Maven, can be changed as per your build tool)
                sh 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy to a server (example with Docker)
                sh 'docker build -t my-image .'
                sh 'docker push my-image'
                // Or use a deployment script/command if needed
            }
        }
    }
}
