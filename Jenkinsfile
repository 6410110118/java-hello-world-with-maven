pipeline {
    agent any

    stages {
        stage('Maven') {
            steps {
                script {
                    // Run Maven inside a Docker container without -it
                    sh 'docker run --rm --name my-maven-project maven:3.9.9 mvn --version'
                }
            }
        }
        stage('Build') {
            steps {
                dir('/var/jenkins_home/myapp') {                
                    script {
                        // Run Maven inside a Docker container without -it
                        //sh 'ls -l'
                        sh 'docker run --rm --name my-maven-project -v "$(pwd):/usr/src/mymaven" -w /usr/src/mymaven maven:3.9.9 mvn clean install'
                    }
                }
            }
        }
    }
}
