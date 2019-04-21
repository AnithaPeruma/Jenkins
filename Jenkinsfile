pipeline {
    stages {
        stage('Initialize') {
            steps {
                //enable remote triggers
                script {
                    properties([pipelineTriggers([pollSCM('')])])
                }
                //define scm connection for polling
                git branch: BRANCH_NAME, credentialsId: 'anithaperuma', url: 'https://github.com/AnithaPeruma/Jenkins.git'
            }
        }
    }
}
