@Library('my-shared-library') _

pipeline {

    agent any 
    stages {
        stage('Git checkout') {
            steps {
                script {
                    gitCheckout(
                        branch : "main",
                        url: "https://github.com/Ramlu/mr-devops-java-app.git",
                        credentialsId: 'github-token'
                    )
                }
            }
        }
    }
}