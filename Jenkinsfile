#!groovy

pipeline {
    agent any

    tools {
        maven "3.6.0"
    }

    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
                sh "cd 'target'"
                sh "java -jar maven-pipeline-demo-1.0-SNAPSHOT.jar"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
