pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/example/repository.git'
            }
        }
        
        stage('Build') {
            steps {
                // Clean and install dependencies
                sh 'mvn clean install'
            }
        }
    }
}
