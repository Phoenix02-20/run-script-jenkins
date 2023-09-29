pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build and Run Python Script') {
            steps {
                // Define the Python environment (you may need to install Python and necessary packages)
                sh 'python3 -m venv venv'
                sh 'source venv/bin/activate'
                // Run your Python script
                sh 'python test.py'
            }
        }
    }
}
