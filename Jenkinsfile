node {
    stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'Sonar';
    withSonarQubeEnv('Sonar') {
      bat "${scannerHome}/bin/sonar-runner.bat"
    }
  } 
}
