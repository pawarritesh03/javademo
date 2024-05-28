pipeline {
    agent { label 'MyFirstLabel' }

    stages {
        stage('checkout the code') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cloud-dev-user/javademo.git']])
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
