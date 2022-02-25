pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                retry(3){
                    sh "command"
                }
                timeout(time:3,unit:"MINUTES"){
                    sh "some command"
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post {
        failure {
            echo "Oh! No!"
        }
        success {
            echo "Oh! Yeah that Success"
        }
    }
}