pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh './gradlew test'
                sh './gradlew dockerBuild'
            }
        }
        stage('push') {
            steps {
                sh './gradlew dockerPush'
            }
        }
    }
}