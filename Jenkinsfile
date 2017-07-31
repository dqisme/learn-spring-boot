pipeline {
    agent { docker 'openjdk:8-jre' }
    stages {
        stage('build') {
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
    }
}