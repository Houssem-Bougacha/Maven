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
               
                    bat 'mvn clean compile'
              
            }
        }
      
        stage('Testing Stage') {
            steps {
                
                    bat 'mvn test'
            
            }
        }
        stage('Install Stage') {
            steps {
        
                    bat 'mvn install'
            
            }
        }
    }
}
