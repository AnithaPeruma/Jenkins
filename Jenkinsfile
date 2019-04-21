pipeline {
    agent any

    stages {

        // Normal Stages

        stage ('success'){
            steps {
                script {
                    currentBuild.result = 'FAILURE'
                }
            }
        }
    }

    post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }

        always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "anitha.perumal@mindtree.com",
                sendToIndividuals: true])
        }
    }
}
