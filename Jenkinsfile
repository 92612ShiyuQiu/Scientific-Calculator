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
  agent any
  tools {
    maven 'Maven 3.3.9'
    jdk 'jdk8'
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
