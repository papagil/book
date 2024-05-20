pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                // Compile the source code of the Maven project
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                // Run the tests of the Maven project
                sh 'mvn test'
            }
        }
        stage('Quality-check') {
            steps {
                // Perform quality checks on the Maven project (e.g., static code analysis, integration tests)
                sh 'mvn verify'
            }
        }
        stage('Package') {
            steps {
                // Package the compiled code into a distributable format (e.g., JAR, WAR)
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
        always {
            echo 'Pipeline finished.'
        }
    }
}

