pipeline{
    agent any
    tools {
        maven 'maven-3.6.3'
    }
    stages{
        stage('Build'){
            steps{
                echo 'Building the app'
            }
        }
        stage('test'){
            steps{
                echo 'Testing the App'
            }
        }
        stage('Deploy for production'){
            when{
                branch 'production'
            }
            steps{
                input message: 'Is test successful?'
                echo 'Test is successful and proceeding for production'
            }
        }
    }
}
