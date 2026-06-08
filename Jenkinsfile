pipeline {
    agent any

    stages {

        stage('Validar Python') {
            steps {
                bat '"C:\\Users\\Home\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" --version'
            }
        }

        stage('Instalar dependencias') {
            steps {
                bat 'pip install pandas'
                bat 'pip install psycopg2-binary'
            }
        }

        stage('Ejecutar procesamiento') {
            steps {
                bat '"C:\\Users\\Home\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" scripts\\procesamiento.py'
            }
        }

        stage('Validación final') {
            steps {
                echo 'Pipeline ejecutado correctamente'
            }
        }
    }
}