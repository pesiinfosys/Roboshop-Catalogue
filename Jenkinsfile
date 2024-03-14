pipeline {
    agent{
        label 'NodeJS'
    }
    // options {
        
    // }
    // environment {

    // }
    // parameters{
        
    // }
    stages{
        stage('Install Dependencies') {
            steps {
                echo "Installing Dependencies"
                sh 'npm install'
            }
        }
        stage('Unit Testing') {
            steps {
                echo "Unit Test is done here"
            }
        }
        stage('Sonar Scanning') {
            steps {
                echo "Sonar Qube Scanning"
                sh 'ls -ltr'
                sh 'sonar-scanner'
            }
        }
        stage('Deploying') {
            steps {
                echo "Deploying...."
                
            }
        }
    }
    // post {
        
    // }
}