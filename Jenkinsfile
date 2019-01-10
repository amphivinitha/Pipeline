pipeline {
    agent {
        docker 'maven:Default'
    }
    stages {
        
        stage("compile") {
            steps {
                bat 'mvn clean compile'
            }
        }
        
        stage("Testing") {
            steps {
                bat 'mvn test'
            }
        }

        stage("Build") {
            steps {
                bat 'mvn package'
            }
        }
    }
}
