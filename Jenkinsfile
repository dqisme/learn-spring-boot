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
        sh 'env'
        sh 'curl -I http://docker.for.mac.localhost:8123'
        sh 'curl -I https://www.baidu.com'
        catchError() {
          sh './gradlew clean'
          sh 'sleep 1000'
          sh 'export GRADLE_OPTS="-Dhttps.proxyHost=docker.for.mac.localhost -Dhttps.proxyPort=8123"; ./gradlew clean'
        }
        
        sleep 10000
      }
    }
    stage('test') {
      steps {
        sh './gradlew cucumber'
      }
    }
  }
  environment {
    GRADLE_OPTS = '-Dhttps.proxyHost=docker.for.mac.localhost -Dhttps.proxyPort=8123'
    JAVA_OPTS = '-XX:ErrorFile=/var/log/java/hs_err_pid%p.log'
  }
}