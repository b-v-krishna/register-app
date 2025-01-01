pipeline{
    agent {
        label 'Jenkins-Agent'
    }
    tools{
        jdk 'Java17'
        maven 'Maven3'
    }
    stages{
        stage('cleanup workspac'){
            steps{
                cleanWs()
            }
        }
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/b-v-krishna/register-app.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        
    }
}
