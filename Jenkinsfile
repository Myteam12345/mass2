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
                cd /var/lib/jenkins/workspace/mass2/target
                cp '/var/lib/jenkins/workspace/mass2/target/mastan2.war' '/home/revathi/Downloads/apache-tomcat-7.0.88/webapps'
            }
        }
    
    }
}
