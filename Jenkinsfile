pipeline {
    agent any
    stages {
        stage("Compile") {
            sh "./gradlew compileJava"
        }
        stage("Unit Test") {
            sh "./gradlew test"
        }
    }
}