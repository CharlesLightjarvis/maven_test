pipeline {
  agent any
  tools {
    jdk 'JDK'
  }
  environment {
    JAVA_HOME = 'C:\\Program Files\\Java\\jdk-17'
  }
  stages {
    stage ('Compile Stage') {
      steps {
        withMaven(maven: 'Maven_3.3.2') {
          bat 'mvn clean compile'
        }
      }
    }
    stage ('Testing Stage') {
      steps {
        withMaven(maven: 'Maven_3.3.2') {
          bat 'mvn test'
        }
      }
    }
    stage ('Install Stage') {
      steps {
        withMaven(maven: 'Maven_3.3.2') {
          bat 'mvn install'
        }
      }
    }
  }
}
