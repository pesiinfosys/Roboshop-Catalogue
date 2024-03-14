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
        stage('clean_workspace_and_checkout_source') {
            steps {
                deleteDir()
                // checkout scm
            }
        }
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
        // stage('Sonar Scanning') {
        //     steps {
        //         echo "Sonar Qube Scanning"
        //         sh 'ls -ltr'
        //         sh 'sonar-scanner'
        //     }
        // }
        stage('Build') {
            steps {
                echo "Application Build"
                sh 'zip -r catalogue.zip node_modules service.js package.json systemd.service'
            }
        }
    }
    // post {
        
    // }
}