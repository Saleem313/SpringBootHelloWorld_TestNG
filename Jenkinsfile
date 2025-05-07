pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "m386"
    }

    stages {
        /*stage('SCM-CheckIns') {
            steps{
                // Get some code from a GitHub repository
                //git 'https://github.com/Saleem313/SpringBootHelloWorld_TestNG.git'

                // Run Maven on a Unix agent.

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }*/
        stage('Test'){
           steps{
               sh "mvn test"
           } 
        }
        stage('Build'){
            steps{
                sh "mvn clean install"
            }
        }
    }
}
