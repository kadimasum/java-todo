pipeline{
    agent any
    tools {
        gradle "gradle"
    }
    stages{
        stage("Cloning repository"){
          steps{
                git branch:'master', url:'https://github.com/NicholasMariga/java-todo.git'
            }
        }
        
        stage("Building code"){
            steps{
                sh "gradle build"
            }
        }
        
        stage("Testing code"){
            steps{
                sh "gradle test"
            }
        }
        stage("Archive"){
            steps{
                sh "echeo 'Archiving the build'"
            }
        }
    }
}
