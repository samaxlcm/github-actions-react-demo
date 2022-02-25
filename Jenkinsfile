pipeline {
    agent {
        label 'jenkins_agent'
    }

    // agent any

    stages {
        environment { 
            registry = "YourDockerhubAccount/YourRepository" 
            registryCredential = 'dockerhub_id' 
            dockerImage = '' 
        }

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

        stage("Test"){
            steps{
                echo "Testing begin testing2"
                sh "pwd"
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