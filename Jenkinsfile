pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'Maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/snehamadhavi757/BoardgameListingWebApp.git'
            }
        }
        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
        stage('Install') {
            steps {
                sh "mvn install"
            }
        }
    }
}
