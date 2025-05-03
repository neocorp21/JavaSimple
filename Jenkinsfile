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
                sh './mvnw clean install'  // Para usar Maven Wrapper
                // sh 'mvn clean install'  // Si tienes Maven instalado
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
