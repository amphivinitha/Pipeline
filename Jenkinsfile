pipeline {
    agent any
    
    triggers {
        cron('H/10 * * * *')
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
