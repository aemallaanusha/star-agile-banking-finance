pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git url: 'https://github.com/aemallaanusha/star-agile-banking-finance/'
                 echo 'github url checkout'
            }
        }
        stage('codecompile with anusha'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile:compile'
            }
        }
        stage('codetesting with anusha'){
            steps{
                sh 'mvn test:test'
            }
        }
        stage('qa with akshat'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('package with akshat'){
            steps{
                sh 'mvn jar:jar'
            }}
 
}
}
