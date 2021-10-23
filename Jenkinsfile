
pipeline {
 agent any

 options {
  skipDefaultCheckout()
 }
 stages {
  stage('SCM') {
   steps {
    checkout scm
   }
  }
    
stage('Checkout Source') {
      steps {
        git url:'https://github.com/katsudoka2/DevopsPfe.git', branch:'main'
      }
    }
   
       

 
 }
 

 
  }
