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
                sh 'make' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        
        stage('Test') {
            steps {
             
                echo 'testing'
            }
        }
        
       
        stage('Deploy') {
            eps {
                echo 'deploy'
            }
        }
    
    }
}
