pipeline {
    agent any
    tools {
        maven "mvn363"
    }
    triggers {
    cron '5 7 * * *'
  }
    
    pipelineTriggers(triggers)
}
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shekar55/maven-project.git'
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
