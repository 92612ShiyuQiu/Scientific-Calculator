node{
  stage('SCM Checkout'){
    git 'https://github.com/92612ShiyuQiu/Scientific-Calculator.git'
  }
  stage('Build'){
    //def mvnHome = tool name: 'maven', type: 'maven'
    //tool(name: 'maven', type:'maven')
    tool name: 'maven', type: 'maven'
    sh "cd Calculator"
    sh "mvn -f /var/lib/jenkins/workspace/build-test-calculator/Calculator/pom.xml clean install"
    //sh "${mvnHome}/bin/mvn clean install"
  }
  stage('Test'){
    sh "mvn -Dtest=CalculatorSpec test"
  }
}
