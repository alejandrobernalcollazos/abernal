// This shows a simple example of how to archive the build output artifacts.
node {
    stage('SonarQube analysis') {
        checkout scm
        def scannerHome = tool 'sonarqube_scanner';
        withSonarQubeEnv('sonarqube_server') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
