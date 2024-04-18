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
            def scannerHome = tool 'sonarqube-jenkins';
            withSonarQubeEnv() {
                sh "./gradlew sonar"
            }
        }
    }
}