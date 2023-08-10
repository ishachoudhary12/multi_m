pipeline {
    agent any
    
    tools{
        jdk 'JAVA'
        maven 'Maven-3.6.3'
    }

    stages {
        stage('GIT Checkout') {
            steps {
               git branch: 'development-1', url: 'https://github.com/ishachoudhary12/multi_m.git'
            }
        }
        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
    }
}
