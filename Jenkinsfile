pipeline {
	agent any
	environment {
		DIRECTORY_PATH = "${WORKSPACE}"
		TESTING_ENVIRONMENT = 'staging'
		PRODUCTION_ENVIRONMENT = 'Junyi Yang'
	}
stages {
        stage('Build') {
            steps {
                echo "Building the code from directory: ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating any necessary artifacts"
            }
        }        
        stage('Test') {
            steps {
                echo "Running tests in ${env.TESTING_ENVIRONMENT} environment"
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
	    }
        stage('Deploy') {
            steps {
                echo "Deploying the application to a testing environment specified by the environment variable"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting for manual approval..."
                //sh 'sleep 10' 
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to the production environment (${env.PRODUCTION_ENVIRONMENT})"
            }
        }
    }
}
