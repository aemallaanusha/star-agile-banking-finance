pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git 'https://github.com/aemallaanusha/star-agile-banking-finance/'
                 echo 'github url checkout'
            }
        }
        stage('codecompile with akshat'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile'
            }
        }
        stage('codetesting with akshat'){
            steps{
                echo 'starting testing'
                sh 'mvn test'
            }
        }
        stage('qa with akshat'){
            steps{
                echo 'starting analysing'
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('package with akshat'){
            steps{
                echo 'starting packaging'
                sh 'mvn package'
            }
        }
        stage('run dockerfile'){
          steps{
               sh 'docker build -t myimg .'
           }
         }
 
    }
}
