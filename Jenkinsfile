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
        stage('metricCheck'){
          steps{
            sh 'mvn cobertura:cobertura -Dcobertura.report.format=xml'
          }
        }
        stage('package'){
          steps{
           sh 'mvn package'
          }
        }
     }
  }
