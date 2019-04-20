pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'start' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true (2)
            }
        }
    }
}
