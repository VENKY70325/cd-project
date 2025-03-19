pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master',url: 'https://github.com/SreeramPavani5/WeatherForecasting.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'pm2 restart app.js'
            }
        }
    }
}
