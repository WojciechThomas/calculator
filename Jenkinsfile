pipeline {
    agent {
        docker {
            image 'openjdk:8-jdk-alpine'
        }
        
    }
    stages {
        stage("Checkout") {
            steps {
                git url: 'https://github.com/WojciechThomas/calculator.git'
            }
        }
    
        stage("Compile") {
            steps {
                sh './gradlew compileJava'
            }
        }
        stage("Test") {
            steps {
                sh './gradlew test'
            }
        }
    }        
}
