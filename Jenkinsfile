pipeline {
    agent any

    environment {
        CI = 'false'  // Disable the CI flag to ignore warnings as errors
    }

    stages {
        stage('Git checkout') {
            steps {
                git 'https://github.com/betawins/Trading-UI.git'
            }
        }

        stage('Install npm prerequisites') {
            steps {
                sh 'npm install'
                sh 'npm run build'
                sh 'timeout 120s npm start'
            }
        }
    }
}
