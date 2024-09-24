pipeline {
        agent none
        stages {
         
          stage("build & 6410110118-sonaqube") {
            agent any
            steps {
              withSonarQubeEnv('6410110118-sonaqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }