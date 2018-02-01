pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '''-v /root/.m2:/root/.m2
'''
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
  }
  environment {
    https_proxy = '10.144.1.10:8080'
  }
}