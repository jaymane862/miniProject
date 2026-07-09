pipeline {
    agent any
    stages {

       stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/jaymane862/miniProject.git'
            }
        }
        stage('Run Tests') {
            steps {
               bat 'java -version'
               bat 'mvn -version'
               bat 'mvn clean test'
            }
        }

     }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
