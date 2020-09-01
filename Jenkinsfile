pipeline {
    agent any
    stages {
        stage("Webhook") {
            steps {
                waitForQualityGate(webhookSecretId: 'jenkins')
            }
        }
        stage('SonarQube analysis 1') {
            steps {
                withSonarQubeEnv('sonarserver'){
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
        stage("Quality Gate 1") {
            steps {
                waitForQualityGate abortPipeline: true
            }
        }
        stage('SonarQube analysis 2') {
            steps {
                sh 'gradle sonarqube'
            }
        }
        stage("Quality Gate 2") {
            steps {
                waitForQualityGate abortPipeline: true
            }
        }
    }
}
