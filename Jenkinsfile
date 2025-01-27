pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building..."
		sh 'python3 --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'python3 -m unittest discover tests' // Run tests directly
            }
        }
    }
}
