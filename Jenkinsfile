@Library('my-shared-library') _

pipeline {

    agent any 
    stages {
        stage('Clean WS') {
            steps {
                cleanWs()
            }
        }
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
        stage('Maven Test') {
            steps {
                script {
                    mvnTest()
                }
            }
        }
    }
}