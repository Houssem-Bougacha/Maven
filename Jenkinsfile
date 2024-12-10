pipeline {
    agent any
    tools {
        jdk 'JDK'
    }
    environment {
        JAVA_HOME = 'C:\\Program Files\\Java\\jdk-21' 
    }
    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven: 'Maven3.9.7 windows') { 
                    bat 'mvn clean compile'
                }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'Maven3.9.7 windows') {
                    bat 'mvn test'
                }
            }
        }
        stage('Install Stage') {
            steps {
                withMaven(maven: 'Maven3.9.7 windows') {
                    bat 'mvn install'
                }
            }
        }
    }
}
