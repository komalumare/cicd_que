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
                deploy adapters: [tomcat8(credentialsId: '8f9e4a48-90b7-4b3e-a2d3-6e6706eb89ae', path: '', url: 'http://localhost:8282/')], contextPath: 'hello', war: '**/*.war'
            }
        }
        stage("enviroment"){
            steps{
                echo "enviroment"
            }
        }
    }
}
