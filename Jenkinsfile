pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'whoami'
        sh 'curl -I http://docker.for.mac.localhost:8123'
        sh 'curl -I https://www.baidu.com'
        sh './gradlew clean'
        sh './gradlew build'
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
}