pipeline {
    agent any
    options {
        skipDefaultCheckout(true)
    }
    
    stages {
        stage('Debug') {
            steps {
                script {
                    sh 'git ls-remote -h https://github.com/Phoenix02-20/run-script-jenkins.git HEAD'
                }
            }
        }
        
        // stage('Build and Run Python Script') {
        //     steps {
        //         // Define the Python environment (you may need to install Python and necessary packages)
        //         sh 'python3 -m venv venv'
        //         sh 'source venv/bin/activate'
        //         //sh 'pip install -r requirements.txt' // If you have requirements for your Python script
                
        //         // Run your Python script
        //         sh 'test.py'
        //     }
        // }
    }
}
