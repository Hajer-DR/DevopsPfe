
pipeline {
 agent any
 environment {
 // registry = "narjess6/devops"
  // This can be nexus3 or nexus2
  //NEXUS_VERSION = "nexus3"
  // This can be http or https
  //NEXUS_PROTOCOL = "http"
  // Where your Nexus is running. In my case:
  //NEXUS_URL = "192.168.0.170:1081"
  // Repository where we will upload the artifact
 // NEXUS_REPOSITORY = "maven-nexus-repo"
  // Jenkins credential id to authenticate to Nexus OSS
 // NEXUS_CREDENTIAL_ID = "nexus-user-credentials"
  /* 
    Windows: set the ip address of docker host. In my case 192.168.99.100.
    to obtains this address : $ docker-machine ip
    Linux: set localhost to SONARQUBE_URL
  */
 // SONARQUBE_URL = "http://192.168.0.170"
 // SONARQUBE_PORT = "9000"
 }
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
    https://github.com/katsudoka2/DevopsPfe/blob/main/deployment.yml
 
         stage('Update Kube Config an deploy to kubernetes'){
            steps {
                withAWS(region:'us-east-2',credentials:'aws-creds') {
                    sh 'aws eks --region us-east-2 update-kubeconfig --name my-eks'   
                    sh 'kubectl apply -f deployment.yml'
                }
            }
        }


 
 }
 

 
  }
