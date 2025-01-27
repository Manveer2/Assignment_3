pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Setting up Python environment...'
                sh 'python3 -m venv venv' // Create virtual environment
                sh './venv/bin/pip install --upgrade pip'
                sh './venv/bin/pip install -r requirements.txt' // Install dependencies
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './venv/bin/python -m unittest discover tests' // Discover and run tests
            }
        }
    }
}
