pipeline {
  agent any
  tools{ jdk 'jdk’ }
  environment { JAVA_HOME = 'C:\\Program Files\\Java\\jdk17' }
  stages {
    stage ('Compile Stage') {
      steps {
        withMaven(maven : 'apache-maven-3.8.8') {
        bat 'mvn clean compile'
      }
}
    stage ('Testing Stage') {
      steps {
        withMaven(maven : 'apache-maven-3.8.8') {
        bat 'mvn test'
        } 
      }
    }
    stage ('Install Stage') {
      steps {
        withMaven(maven : 'apache-maven-3.8.8') {
        bat 'mvn install'
        } 
      } 
    } 
  }
}
