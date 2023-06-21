pipeline {
    agent any
    
    tools{
        jdk 'java'
        maven 'Maven'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/adhikarirahul666/Petclinic.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn clean compile"
            }
        }
        
        stage('Build') {
            steps {
               sh "mvn clean package -DskipTests=true"
            }
        }
        
        
        
        
    }
}
