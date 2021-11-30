pipeline{
    agent any
    stages{
        stage('Clean stage'){
            steps{
                sh 'docker ps'
            }
        }
        stage('Build stage'){
            steps{
                sh 'docker build -t vipulgola/webserver:0.0.1 .'
            }
        }
        stage('package'){
            steps{
                sh 'docker push vipulgola/webserver:0.0.1'
            }
        }
        stage('package upload'){
            steps{
                sh 'docker run --rm -p 80:80 vipulgola/webserver:0.0.1'
            }
        }
    }
}
