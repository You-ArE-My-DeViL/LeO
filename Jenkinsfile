pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code repository
                git 'https://github.com/You-ArE-My-DeViL/LeO.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build the Maven project
                sh 'mvn clean package'
            }
        }
    }
    
    post {
        success {
            // Archive the built artifacts
            archiveArtifacts 'target'
        }
        failure {
            // Send a notification or perform actions in case of build failure
            echo 'Build failed!'
        }
    }
}

