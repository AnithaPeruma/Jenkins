pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                sh 'mvn clean install -Dmaven.test.failure.ignore=true'
            }
        }
    }
    post {
        always {
            archive "**/**/*"
            junit 'test-report.xml'
        }
    }
}
