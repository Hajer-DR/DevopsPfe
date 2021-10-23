
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
   
   stage('Update Kube Config an deploy to kubernetes'){
            steps {
                withAWS(region:'us-west-1',credentials:'aws-creds') {
                    sh 'aws eks --region us-west-1 update-kubeconfig --name my-eks'   
                    sh 'kubectl apply -f deployment.yml'
                }
            }
        }      

 
 }
 

 
  }
