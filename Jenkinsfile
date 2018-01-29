pipeline {
    agent {
        kubernetes {
            label 'jenkins-demo'
                containerTemplate {
                    name 'dind-jdk8-maven3'
                        image 'eu.gcr.io/jenkins-demo/dind-jdk8-maven3:v4'
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
