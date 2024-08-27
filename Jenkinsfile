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
        stage("email"){
            emailext body: 'hii your jenkins pipeline is faild', subject: 'regarding test fail or piprline fail', to: 'te415606@gmail.com'
            
        }
    }
}
