pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "/mvn test"
            }
        }
        stage('--package--') {
            steps {
                agent { label 'slave-node' }
                sh "mvn package"
            }
        }
    }
}
