pipeline{
    agent any
    
    stages{
       stage("code clone"){
           steps{
               git url:"https://github.com/AsadJaved123/resume.git", branch:"main"
           }
       } 
       stage("Build image"){
           steps{
               sh "docker build -t resume ."
           }
       }
       stage("Deploy"){
           steps{
               sh "docker-compose down && docker-compose up -d"
           }
       }
    }
}
