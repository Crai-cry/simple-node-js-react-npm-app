pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { image 'node:18-alpine' }
            }
            steps {
                echo 'Устанавливаю зависимости...'
                sh 'node --version'
                sh 'npm --version'
                sh 'npm install'
            }
        }
        stage('Test') {
            agent {
                docker { image 'node:18-alpine' }
            }
            steps {
                echo 'Запускаю тесты...'
                sh 'npm test'
            }
        }
    }

    post {
        success { echo 'Пайплайн прошёл успешно' }
        failure { echo 'Что-то сломалось' }
    }
}
