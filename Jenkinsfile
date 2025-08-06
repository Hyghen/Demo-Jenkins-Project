pipeline {
    agent any
    tools {
        maven 'Maven' 
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
            
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }   
        stage('Deploy to Prod') {
            steps {
                deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcatcredentials', path: '', url: 'http://192.168.1.8:8080')], contextPath: '/app', war: '**/*.war'  
            }
        }         
    }
}
