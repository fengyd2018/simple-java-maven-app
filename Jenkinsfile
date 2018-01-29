pipeline {
    agent {
        kubernetes {
            label 'jenkins-demo'
                containerTemplate {
                    name 'maven3'
                        image 'maven:3-alpine'
                        ttyEnabled true
                        command 'cat'
                }
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
