pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
      args '--env https_proxy=docker.for.mac.localhost:8123'
    }
    
  }
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