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
                sh 'make check || true' 
                junit '**/target/*.xml' 
            }
        }
        
       
        stage('Deploy') {
            when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            steps {
                sh 'make publish'
            }
        }
    
    }
}
