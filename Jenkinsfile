node{
  stage('SCM Checkout'){
    git 'https://github.com/92612ShiyuQiu/Scientific-Calculator.git'
  }
  stage('Build'){
    //def mvnHome = tool name: 'maven', type: 'maven'
    tool(name: 'maven', type:'maven')
    sh "cd Calculator"
    //sh "${mvnHome}/bin/mvn clean install"
  }
}
