pipeline {
    agent any
    
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
        stage('Checkout') {
            steps {
                // Checkout your source code repository (e.g., Git)
                checkout scm
            }
        }
        
        stage('Build and Run Python Script') {
            steps {
                // Define the Python environment
                script {
                    // Create a virtual environment
                    sh 'python3 -m venv venv'
                    
                    // Activate the virtual environment
                    sh 'source venv/bin/activate'
                    
                    // Install required Python packages (if you have a requirements.txt file)
                    // sh 'pip install -r requirements.txt'
                    
                    // Run your Python script
                    sh 'python test.py'
                }
            }
        }

    }
}
