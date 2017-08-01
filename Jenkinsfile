pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
      args '--env https=docker.for.mac.localhost:8123'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'env'
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