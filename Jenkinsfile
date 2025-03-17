pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/frankyu02/maven-samples.git', branch: 'master')
      }
    }

    stage('build steps') {
      steps {
        sh 'mvn clean install'
        sh 'mvn clean'
        sh 'mvn test'
        sh 'mvn verify'
      }
    }

  }
}
