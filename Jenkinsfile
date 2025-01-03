def gv


pipeline {  
    agent any
    tools {
        maven 'Maven-3.9.2'
    }
    
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }

        stage("Test") {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for branch ${BRANCH_NAME}"
                }
            }
        }
        
        
        
        stage("build jar") {
            steps {
                script {
                    buildJar()
                }
            }
        }

        stage("build image") {
            steps {
                script {
                    buildImage()
                }
            }
        }

        stage("deploy App") {
            steps {
                script {
                    gv.deployApp()
                }
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Please check the logs for details."
        }
    }
}
