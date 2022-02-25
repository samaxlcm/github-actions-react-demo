pipeline {
    // agent {
    //     label 'jenkins_agent'
    // }

    agent any

    stages {
        stage('Build') {
            steps {
                retry(3){
                    sh "ls -l"
                }
                timeout(time:3,unit:"MINUTES"){
                    sh "ls -l"
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