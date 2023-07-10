pipeline {
    agent {
        node {
            label 'maven-agent'
        }
    }
    
environment {
    PATH = "/opt/apache-maven-3.9.3/bin:$PATH"
}
    
    stages{
        stage('clone code') {
            steps {
                git branch: 'main', url: 'https://github.com/Git-Manee/sahealthdomainprjct.git'
            }
        }
    }
    stages{
        stage('Build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
