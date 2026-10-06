pipeline{
    agent any
    stages{
        stage("Clone repo"){
            steps{
                git url: 'https://github.com/kadimasum/java-todo', branch: 'master'
            }
        }
        stage("Build Code"){
            steps{
                sh "./gradlew build"
            }
        }
        stage("Test Code"){
            steps{
                sh "./gradlew test"
            }
        }
    }
}