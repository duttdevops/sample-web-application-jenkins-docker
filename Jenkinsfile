node{
   stage('SCM Checkout'){
     git branch:'main',url:'https://github.com/duttdevops/sample-web-application-jenkins-docker'
   }
   stage('Build'){
      // declaring maven home path
      def mvnHome =  tool name: 'Maven3', type: 'maven'
      sh "${mvnHome}/bin/mvn clean package"
   }
   stage('docker push'){
   sh 'docker build -t webapp:latest .'
   sh "docker login -u 'duttdevops' -p 'Gr3yf@!c0n'"
   sh 'docker push duttdevops/ksd:latest'
   }
}
