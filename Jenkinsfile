pipeline {
    environment {
        DIRECTORY_PATH = 'path/to/your/code'
        TESTING_ENVIRONMENT = 'NameOfTestingEnvironment'
        PRODUCTION_ENVIRONMENT = 'YourName'
    }
    stages {
        stage('Build') {
            steps {
                echo 'fetch the source code from the directory path specified by the environment variable'
                echo 'compile the code and generate any necessary artifacts'
            }
        }
        stage('Test') {
            steps {
                echo 'unit tests'
                echo 'integration tests'
            }
        }
        stage('Code Quality Check') {
            steps {
                echo 'check the quality of the code'
            }
        }
        stage('Deploy') {
            steps {
                echo "deploy the application to the testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                sleep time: 10, unit: 'SECONDS'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "deploy the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
