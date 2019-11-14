pipeline {
  agent {
    docker {
      image 'maven:3-jdk-8'
      args '-v /var/jenkins_home/.m2:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests -Duser.home=/var/maven clean package'
      }
    }

  }
}