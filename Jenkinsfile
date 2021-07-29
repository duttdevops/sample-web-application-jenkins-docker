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
   sh 'docker build -t duttdevops/ksd:latest .'
   sh "docker login -u 'duttdevops' -p 'Gr3yf@!c0n'"
   sh 'docker push duttdevops/ksd:latest'
   }
   stage('docker pull')
   sh "docker login -u 'duttdevops' -p 'Gr3yf@!c0n'"
   sh 'docker pull duttdevops/ksd:latest'
   sh 'docker run -d duttdevops/ksd:latest -p 8082:8080'
}
