pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'env'
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