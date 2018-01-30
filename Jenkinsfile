pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '''-v /root/.m2:/root/.m2
-w /var/jenkins_home/workspace
-v  /var/jenkins_home/workspace:/var/jenkins_home/workspace'''
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