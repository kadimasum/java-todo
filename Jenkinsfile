pipeline{
    agent any
    
    stages{
        stage("Clone repo"){
            steps{
                git branch:'master', url: 'https://github.com/kadimasum/java-todo.git'
            }
        }
        
        stage("Build code"){
            steps{
                sh './gradlew build'
            }
        }
        
        stage("Test code"){
            steps{
                sh './gradlew test'
            }
        }
    }
}