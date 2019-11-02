// This shows a simple example of how to archive the build output artifacts.
node {
    stage('SonarQube analysis') {
        checkout scm
        def scannerHome = tool 'SonarScanner 4.0';
        withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
