// This shows a simple example of how to archive the build output artifacts.
node {
    stage "Build"
    // Checkout repository
    checkout scm
    // Make the output directory.
    sh "echo I am building LEITO PICHONI AND YAIL PERALTA"
    sh "docker build -t frontend:v1 ."
    
    stage "Unit Tests"
    
    // Make the output directory.
    sh "echo I am executing unittests for LEITO PICHONI AND YAIL PERALTA"
    
    stage "Static Code Analysis"
    
    // Make the output directory.
    sh "echo Static Code Analysis my friends LEITO PICHONI AND YAIL PERALTA"
    
    stage "Automated Testing"
    
    // Make the output directory.
    sh "echo I am executing the automated tests LEITO PICHONI AND YAIL PERALTA"
 
    stage "Running Chayane page "
    // Eliminar el contenedor que esta corriendo actualmente
    try {
          sh "docker rm leo -f"
        }
        catch (exc) {
            echo 'No pude borrar el contenedor'
        }

    // Subir el contenedor nuevo
    sh "docker run -d -p 8888:80 --name leo frontend:v1 "

}
