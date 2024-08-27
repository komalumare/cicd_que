pipeline {
    agent any 

    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/komalumare/cicd_que.git'
            }
        }
        stage('build'){
            steps{
                bat "javac hello.java"
            }
        }
        stage("deploy"){
            steps{
                bat "java hello"
            }
        }
        stage("unit testing"){
            steps{
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
            }
        }
    }
}
