pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn --version'
                dir ('ToolsQa'){
                    sh 'ls '
                    sh 'pwd'
                    sh 'mvn clean'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                dir ("ToolsQa"){
                    sh 'mvn test -Dtest=ToolsQaTest test'
                }               	
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}