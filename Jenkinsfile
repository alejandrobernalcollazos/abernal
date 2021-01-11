// This shows a simple example of how to archive the build output artifacts.
node {
/*
    stage('SonarQube analysis') {
        checkout scm
        def scannerHome = tool 'sonarqube_scanner';
        withSonarQubeEnv('sonarqube_server') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
*/

    stages {
        stage('Continuous Integration') {
          checkout scm
          steps{
            echo 'Ejecutando el proceso de integración continua'
            sh 'docker build -t alejandro .'
            sh 'docker run -p 8888:80 alejandro'
          }
        }
    }
}
