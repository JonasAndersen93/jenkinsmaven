pipeline {
    agent any
    stages {
        stage('Clone repo and clean'){
            steps{
                sh 'git clone https://github.com/JonasAndersen93/jenkinsmaven.git'
                sh 'mvn clean -f jenkinsmaven'

            }
        }
        stage('Test'){
            steps{
                sh 'mvn test -f jenkinsmaven'
            }
        }
        stage('Deploy'){
            steps{
                sh 'mvn package -f jenkinsmaven'
            }
        }
    }
}