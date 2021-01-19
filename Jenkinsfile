pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git 'https://github.com/jkasinat/java-rest-api-calculator.git'
        sh './mvnw clean compile'
      }
    }

    stage('Test') {
      steps {
        sh './mvnw test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }

  }
}