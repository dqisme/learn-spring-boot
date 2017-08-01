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
  environment {
    https_proxy = '127.0.0.1:1080'
    HTTPS_PROXY = '127.0.0.1:1080'
  }
}