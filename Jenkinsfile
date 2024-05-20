pipeline {
    agent any
    stages {
        stage('Compile') {
            steps { 
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps { 
                sh 'mvn test'
            }
        }


	stage('Quality-check') {
            steps {
                sh 'mvn verify'
            }
        }
	

        stage('package') {
            steps { 
                sh 'mvn package'
            }
        }
    }
}
