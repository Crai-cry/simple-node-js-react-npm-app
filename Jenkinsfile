pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Устанавливаю зависимости...'
               
            }
        }
        stage('Test') {
            steps {
                echo 'Запускаю тесты...'
                
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
