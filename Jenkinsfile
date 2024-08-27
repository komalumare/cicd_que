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
        stage("tomcat"){
            steps{
                echo "hii from tomcat"
            }
        }
        stage("enviroment"){
            steps{
                echo "enviroment"
            }
        }
    }
}
