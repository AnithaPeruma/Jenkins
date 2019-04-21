pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('archive') {
      steps {
        parallel(
          "Junit": {
            junit 'target/surefire-reports/*.xml'
            
          },
          
        )
      }
    }
  }
}
