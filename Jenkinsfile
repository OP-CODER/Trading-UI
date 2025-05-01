pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                // Get the code from the GitHub repository
                git 'https://github.com/betawins/Trading-UI.git'
            }
        }

        stage('Install npm prerequisites') {
            steps {
                // Install npm dependencies
                sh 'npm install'

                // Build the project
                sh 'npm run build'

                // Start the project
                sh 'npm start'
            }
        }
    }
}
