pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh '''
                ls
                date
                cal
                pwd
                '''
            }
        }
            
        stage('Build') {
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
