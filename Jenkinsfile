pipeline {
    agent any
    options {
        skipDefaultCheckout(true)
    }
    
    stages {
        stage('Debug') {
            steps {
                script {
                    sh 'ls -l /var/lib/jenkins/workspace/script_master'  // Check workspace permissions
                    sh 'whoami'  // Check current user
                    sh 'id'  // Display user and group information
                    checkout scm
                    sh 'ls -l /var/lib/jenkins/workspace/script_master'  // Check workspace permissions again
                }
            }
        }
    }
}
