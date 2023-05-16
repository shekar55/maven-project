pipeline {
    agent any
    tools {
        maven "mvn363"
    }
    def triggers = []
if (env.BRANCH_NAME == "master) {
    triggers << cron('H H(0-2) * * *')
}
properties (
    [
        pipelineTriggers(triggers)
 
    ]
)
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
