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
  stage('Static Analysis'){
    sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dlicense.skip=true -Dsonar.login="8d91ed7887f282e33c27ba8e2f481a185abcd1b4" '
  }
  stage('Test'){
    sh "mvn -f /var/lib/jenkins/workspace/build-test-calculator/Calculator/pom.xml -Dtest=CalculatorSpec test"
  }
}
