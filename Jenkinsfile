pipeline{
    agent any
    stages {
        stage("Clone repo"){
            steps{
                git url: 'https://github.com/kadimasum/java-todo.git', branch: 'master'
            }
        }
        stage("Build Repo"){
            steps{
                sh "./gradlew build"
            }
        }
        stage("Test code"){
            steps{
                sh "./gradlew test"
            }
        }
    }
}