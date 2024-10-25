pipeline {
    agent any
    
    tools{
        jdk 'jdk17'
        maven 'maven 3'
    }

    stages {
        stage('Git Checkout') {
            steps {
               git branch: 'feature/2', url: 'https://github.com/rub3nius/Petclinic.git'
            }
        }
         stage('Compile') {
            steps {
              sh "mvn clean compile"
            }
        }
        stage('Build') {
            steps {
              sh "mvn clean package -DskipTest=true"
            }
        }
        
    }
}
