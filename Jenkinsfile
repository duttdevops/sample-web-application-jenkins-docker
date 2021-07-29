pipeline {

	agent {
	stages{
		stage('SCM Checkout'){
			
			git branch: 'main', 
			url: 'https://github.com/duttdevops/sample-web-application-jenkins-docker.git'
			
				}
		stage('Build Maven'){
			
				def mvn= tool name: 'Maven3', type: 'maven'
				sh " ${mvn}/bin/mvn clean package "
		
			
			
		}
	
	
	
	}
	}



}
