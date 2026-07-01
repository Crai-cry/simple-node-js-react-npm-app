pipeline {
    agent any

    stages {
        stage('Pre'){
            steps{
                sh "apt install node"
                sh "apt install npm"
            }
        }
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
                sh 'npm run test-that-does-not-exist'
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
