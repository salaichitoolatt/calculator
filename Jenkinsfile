pipeline {
    agent any
    stages {
        stage("Compile") {
            steps {
                sh "./gradlew compileJava"
            }
        }
        stage("Unit Test") {
            steps {
                sh "./gradlew test"
            }
        }
        stage('SonarQube Analysis') {
            withSonarQubeEnv() {
                sh "./gradlew sonar"
            }
        }
    }
}