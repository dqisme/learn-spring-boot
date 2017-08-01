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