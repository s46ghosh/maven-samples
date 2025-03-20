pipeline {
  agent any
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  stages {
    stage('Check Out') {
      steps {
        git(url: 'https://github.com/s46ghosh/maven-samples.git', branch: 'master')
      }
    }

    stage('Clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Verify') {
      steps {
        sh 'mvn verify'
      }
    }
  }
}
