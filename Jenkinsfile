pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

       stage('Build') {
           steps {
               script {
                   sh 'chmod +x ./mvnw'
                   sh './mvnw clean install'
               }
           }
       }


        stage('Test') {
            steps {
                // Ejecutar pruebas si es necesario
                sh './mvnw test'  // Para Maven
                // sh 'mvn test'  // Si tienes Maven instalado
            }
        }

        stage('Deploy') {
            steps {
                // Puedes agregar los pasos para despliegue si es necesario
                echo 'Desplegando el proyecto...'
            }
        }
    }
}
