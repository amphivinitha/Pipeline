pipeline {
    agent any
    stages {
        
        stage("compile") {
            steps {
                withMaven(maven: 'Default') {
                    bat 'mvn clean compile'
                }
            }
        }
        
        stage("Testing") {
            steps {
                withMaven(maven: 'Default') {
                    bat 'mvn test'
                }
            }
        }

        stage("Build") {
            steps {
                withMaven(maven: 'Default') {
                    bat 'mvn package'
                }
            }
        }
    }
}
