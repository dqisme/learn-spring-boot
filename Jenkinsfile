pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'env'
        sh 'pwd'
        sh 'sleep 100000'
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