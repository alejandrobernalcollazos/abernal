// This shows a simple example of how to archive the build output artifacts.
node {
    stage('Sonarqube') {
        environment {
            scannerHome = tool 'SonarScanner 4.0'
        }
        steps {
            withSonarQubeEnv('sonarqube') {
                sh "${scannerHome}/bin/sonar-scanner"
            }
            timeout(time: 10, unit: 'MINUTES') {
                waitForQualityGate abortPipeline: true
            }
        }
    }
}
