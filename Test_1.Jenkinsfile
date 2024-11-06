groovy
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    echo 'Checking out code...'
                    // Клонируем репозиторий
                    checkout scm
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                    // Здесь можете добавить команду сборки вашего проекта
                    // Например, "mvn clean install", "npm install", etc.
                    sh 'sleep 10' // Имитация длительной сборки
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    // Здесь может быть ваша команда тестирования
                    // Например, "mvn test", "npm test", etc.
                    sh 'sleep 15' // Имитация длительного тестирования
                }
            }
        }

        stage('Post-Processing') {
            steps {
                script {
                    echo 'Performing post-processing...'
                    // Результаты тестирования, отчеты и т. д.
                    // Здесь можно добавить задержку для имитации обработки результатов
                    sh 'sleep 5' // Имитация некоторой работы
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
        always {
            echo 'Cleaning up...'
        }
    }
}
