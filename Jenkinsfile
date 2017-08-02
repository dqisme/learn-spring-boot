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
        catchError() {
          sh './gradlew clean'
        }
        
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
}