// This shows a simple example of how to archive the build output artifacts.
/*
node {

    stage('SonarQube analysis') {
        checkout scm
        def scannerHome = tool 'sonarqube_scanner';
        withSonarQubeEnv('sonarqube_server') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }

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
*/

pipeline {
    agent any
    stages {
        stage('Imprimir mensaje de bienvenida') {
            steps {
                echo 'Hola Clase de DevOps de 2021 :D'
            }
        }
        stage('Creando nuevo archivo') {
            steps {
                sh 'touch nuevoarchivo.txt'
            }
        }
        stage('Buil y ejecución de contenedor de docker') {
            steps {
                sh 'docker stop alejandrobernal'
                sh 'docker rm alejandrobernal'
                sh 'docker rmi alejandro'
                sh 'docker build -t alejandro .'
                sh 'docker run --name alejandrobernal -d -p 8888:80 alejandro'
            }
        }
    }
}
