pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean install'
        archiveArtifacts '/target/SpringBootHelloWorld_TestNG-*.jar'
      }
    }

  }
  tools {
    maven 'm386'
  }
}