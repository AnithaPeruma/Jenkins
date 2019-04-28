pipeline {
    agent any
    stages {
        stage ('SCM') {
            steps {
                git branch: 'master', url: "https://github.com/AnithaPeruma/Jenkins.git"
            }
        }

       stage ('SonarQube Analysis'){
steps{

withSonarQubeEnv('Sonar') {
sh 'mvn clean install sonar:sonar'

}
}
}
}
}
