pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'run' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true (2)
            }
        }
    }
}
