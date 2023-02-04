pipeline{
   agent any
      stages{
        stage('git checkout'){
          steps{
           git 'https://github.com/sree9048/gitdemo.git'
          }
        }
        stage('compile'){
          steps{
           sh 'mvn compile'
          }
        }
        stage('codeReview'){
          steps{
           sh 'mvn pmd:pmd'
          }
        }
        stage('unitTest'){
          steps{
           sh 'mvn test'
          }
        }
        stage('package'){
          steps{
           sh 'mvn package'
          }
        }
     }
  }
