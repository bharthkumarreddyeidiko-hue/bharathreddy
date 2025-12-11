pipeline {
    agent { label 'Agent-1' }

    tools {
        jdk 'java-17'
        maven 'MAVEN-3.9'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
    }
}
