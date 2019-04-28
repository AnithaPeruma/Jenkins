node {
  stage('SCM') {
    git 'https://github.com/AnithaPeruma/Jenkins.git'
  }
 stage('Sonarqube') {
    environment {
        scannerHome = tool name: 'Sonar', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
    }

    steps {
        withSonarQubeEnv('Sonar') {
            sh "${scannerHome}/bin/sonar-scanner"
        }

        timeout(time: 10, unit: 'MINUTES') {
            waitForQualityGate abortPipeline: true
        }
    }
}
}
