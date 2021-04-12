//node{
  //stage('SCM Checkout'){
    //git 'https://github.com/92612ShiyuQiu/Scientific-Calculator.git'
  //}
  //stage('Build'){
    //def mvnHome = tool name: 'maven', type: 'maven'
    //tool(name: 'maven', type:'maven')
    //sh "cd Calculator"
    //sh "${mvnHome}/bin/mvn clean install"
  //}
//}
pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }
  }
  stages{
    stage('Build'){
      steps{
        sh 'cd Calculator'
        sh 'mvn clean install'
      }
    }
  }
}
