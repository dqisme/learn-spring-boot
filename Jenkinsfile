pipeline {
  agent {
    docker 'openjdk:8-jre'
  }
  stages {
    stage('build') {
      steps {
        sh 'curl -I https://www.google.com'
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
}