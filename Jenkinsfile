pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'complie source code'
		withMaven(maven: 'MAVEN3.6.3'){
		sh 'mvn clean install'
		}
            }
        }
        stage('Test') {
            steps {
               withMaven(maven: 'MAVEN3.6.3'){
		sh 'mvn test' 
            }
        }
        stage('Deploy') {
            steps {
                withMaven(maven: 'MAVEN3.6.3'){
                sh 'mvn deploy'
            }
        }
    }
}
