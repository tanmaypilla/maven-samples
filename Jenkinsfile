pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/tanmaypilla/maven-samples', branch: 'master')
      }
    }

    stage('test') {
      agent any
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}
