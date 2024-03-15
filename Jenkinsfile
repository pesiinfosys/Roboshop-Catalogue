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
        stage('cloaning') {
            steps {
                git(
                    url: "https://github.com/pesiinfosys/Roboshop-Catalogue.git",
                    branch: "master",
                    
                    // changelog: true,
                    // poll: true
                )
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
        stage('artifact_upload') {
            steps {
                    nexusArtifactUploader(
                        nexusVersion: 'nexus3',
                        protocol: 'http',
                        nexusUrl: '44.203.218.18:8081',
                        groupId: 'com.roboshop',
                        version: 1.0.0,
                        repository: 'catalogue',
                        credentialsId: 'nexus-auth',
                        artifacts: [
                            [artifactId: roboshop,
                            classifier: '',
                            file: 'catalogue.zip',
                            type: 'zip']
                        ]
                    )
            }
        }
        
    }
    // post {
        
    // }
}
