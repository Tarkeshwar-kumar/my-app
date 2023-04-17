pipeline {
    agent any
    stages {
        stage('---clean---') {
            agent { label 'built-in' }
            steps {
                
                sh "mvn clean"
            }
        }
        stage('--test--') {
            agent { label 'built-in' }
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
