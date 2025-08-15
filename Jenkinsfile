pipeline {
    agent any

    tools {
        maven 'Maven3' 
        jdk 'Java17'   
    }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/kapoor-prince/dummy-httpd.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
