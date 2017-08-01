pipeline {
  agent {
    docker 'openjdk:8-jre'
  }
  stages {
    stage('build') {
      steps {
        sh 'curl -I https://www.baidu.com'
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
}