pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Устанавливаю зависимости...'
                sh 'node --version'
                sh 'npm --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Запускаю тесты...'
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Пайплайн прошёл успешно'
        }
        failure {
            echo 'Что-то сломалось'
        }
    }
}
