pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/6410110118/java-hello-world-with-maven.git'
                bat "npm install"
            }
        }

        stage('Scan') {
            steps {
                withSonarQubeEnv(installationName: 'sq1') {
                    bat "npm install sonar-scanner"
                    bat 'npx sonar-scanner -X -X -Dsonar.projectKey=6410110118-sonarqube'
                }
            }
        }
    }
}