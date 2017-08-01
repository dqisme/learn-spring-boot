pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
      args '--env https_proxy=http://docker.for.mac.localhost:8123 --env HTTPS_PROXY=http://docker.for.mac.localhost:8123'
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
  environment {
    https_proxy = 'http://docker.for.mac.localhost:8123'
    HTTPS_PROXY = 'http://docker.for.mac.localhost:8123'
  }
}