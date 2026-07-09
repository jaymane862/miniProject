pipeline {
    agent any
    stages {

      
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
