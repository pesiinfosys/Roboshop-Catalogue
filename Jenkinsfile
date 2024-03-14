pipeline {
    agent{
        label 'Agent-1'
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
    }
    // post {
        
    // }
}