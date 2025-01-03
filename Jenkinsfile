pipeline {   
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "Testing the application...."
                    echo "Sending message about app test"
                }
            }
        }
        
        stage("build") {
            steps {
                script {
                    echo "Building the application...."
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    echo "Deploying the application...."
                }
            }
        }               
    }
} 
