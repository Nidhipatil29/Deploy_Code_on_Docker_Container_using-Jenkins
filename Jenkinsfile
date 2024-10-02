
     pipeline {
         agent any
         stages {
             stage('Clone repository') {
                 steps {
                       git branch : 'main' , url:'https://github.com/Nidhipatil29/Deploy_Code_on_Docker_Container_using-Jenkins.git'

                       sh 'ls -a'

                 }
             }
             
             stage('Build Docker Image') {
                 steps {
                     sh 'docker build -t mywebapp .'
                 }
             }
             stage('Deploy to Docker') {
                 steps {
                     sh 'docker run -d -p 8081:8080 mywebapp'
                 }
             }
         }
     }
     
