pipeline {
    agent any
    tools {
        maven "mvn363"
    }
    triggers {
    def triggers = []
    if (env.BRANCH_NAME == "master") {
        triggers << cron('54 16 * * *')
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
