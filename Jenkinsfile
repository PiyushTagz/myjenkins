pipeline {
    agent any
    environment {
        PATH = "/opt/maven/bin:$PATH"
    }
    stages {
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'master', url: 'https://github.com/PiyushTagz/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
