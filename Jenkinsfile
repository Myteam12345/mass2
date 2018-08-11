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
                mvn install package
            }
        }
        
        stage('Test') {
            steps {
                echo 'testing....'
            }
        }
        
        stage('Release') {
            steps {
                echo 'Releasing....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
