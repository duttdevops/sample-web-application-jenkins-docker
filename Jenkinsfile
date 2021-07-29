node{
   stage('SCM Checkout'){
     git branch:'main',url:'https://github.com/duttdevops/sample-web-application-jenkins-docker'
   }
   stage('Build'){
      // declaring maven home path
      def mvnHome =  tool name: 'maven3', type: 'maven'
      sh "${mvnHome}/bin/mvn clean package"
   }
}
