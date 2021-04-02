pipeline {
    agent any

    stages {
        
        stage('Clean'){
            steps{
                cleanWs()
            }
        }
        
        stage('Source') {
            steps{
                git(
                        url: 'https://github.com/libane97/rest-api-calculator-java.git',
                        branch: 'main'
                    ) 
            }
        }
          stage('Compilation'){
            steps{
                bat 'mvnw compile'
            }
        }
        stage('Test Unitaire'){
            steps{
                bat 'mvnw test'
            }
        }
        
        stage('Test Sonar'){
            steps{
                bat 'mvnw sonar:sonar'
            }
        }
        
    }
    

}
