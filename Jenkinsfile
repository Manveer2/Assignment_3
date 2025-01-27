pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'pip install --user -r requirements.txt' // Install dependencies globally for the user
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'python -m unittest discover tests' // Run tests directly
            }
        }
    }
}
