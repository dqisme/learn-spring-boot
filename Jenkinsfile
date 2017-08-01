pipeline {
  agent {
    docker 'openjdk:8-jre'
  }
  stages {
    stage('build') {
      steps {
        sh 'curl -I https://services.gradle.org/distributions/gradle-3.5-rc-2-bin.zip'
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
}