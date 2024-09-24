pipeline {
        agent none
        // tools {
        //   maven '6410110118-sonaqube-maven' // กำหนดชื่อ Maven ที่ได้ตั้งค่าไว้ใน Jenkins
        //   sonarRunner '6410110118-sonaqube-tool'
        // }
        stages {
         
          stage("build & 6410110118-sonaqube-installation") {
            agent any
            steps {
              withSonarQubeEnv('6410110118-sonaqube-installation') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }