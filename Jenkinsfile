pipeline {
    agent { docker 'openjdk:8-jre' }
    stages {
        stage('build') {
            steps {
                sh './gradlew build --info'
            }
        }
        stage('test') {
            steps {
                sh './gradlew cucumber'
            }
        }
    }
}