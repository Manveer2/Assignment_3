pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Create a virtual environment
                sh 'python3 -m venv venv'
                // Activate the virtual environment and install dependencies
                sh './venv/bin/pip install -r requirements.txt'
            }
        }
	stage('Vulnerability Scan') {

    	    steps {

        	sh '/usr/local/bin/trivy image thirsty_khorana'

   	    }

	}
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run tests within the virtual environment
                sh './venv/bin/python3 -m unittest discover Tests'
            }
        }
    }
}
