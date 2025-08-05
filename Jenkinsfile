pipeline {
    agent any
    tools {
        maven 'Maven' 
    }

    stages {
        stage('Build') {
            steps {
                sh '''
                ls
                date
                cal
                pwd
                mvn --version
                '''
            }
        }
            
        stage('Test') {
            steps {
                echo 'Hello World'
                sh 'sleep 10'
            }
        }   
        stage('Deploy to pre-prod') {
            steps {
                echo 'Hello World'
            }
        }   
        stage('Deploy to prod') {
            steps {
                echo 'Hello World'
                sh 'sleep 10'
            }        
        }
    }
}
