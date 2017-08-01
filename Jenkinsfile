pipeline {
    agent { docker 'openjdk:8-jre' }
    stages {
        stage('build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('test') {
            steps {
                sh './gradlew cucumber'
            }
        }
    }
}