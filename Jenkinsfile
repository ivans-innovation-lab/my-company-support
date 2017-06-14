pipeline {
    agent any
    tools { 
        maven 'maven-3' 
    }
    stages {
        stage ('Build') {
            when {
                branch 'feature/*'
            }
            steps {
                sh 'mvn clean install'
            }
        }
        stage ('Build & Deploy artifact') {
            when {
                branch 'master'
            }
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
