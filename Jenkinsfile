pipeline {
    agent any

    stages {
        stage('Checout the Code') {
            steps {
                echo 'checking out the code.'
            }
        }
        stage('build') {
            steps {
                sh 'mvn install package'
                
            }
        }
        
        stage('Test') {
            steps {
             
                echo 'testing'
            }
        }
        
       
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    
    }
}
