pipeline {
    agent { label 'MyFirstLabel' }
    parameters {string defaultValue: 'master', name: 'branch_name'}
    stages {
        stage('checkout the code') {
            steps {
                git branch: "$branch_name", url: 'https://github.com/pawarritesh03/javademo.git'
            }
        }
        
        stage('build the code') {
            steps {
                sh 'mvn clean install'
            }
        }
        
        stage('clean the ws') {
            steps {
                cleanWs()
            }
        }
        
    }
}
