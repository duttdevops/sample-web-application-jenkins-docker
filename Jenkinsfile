pipeline {
agent 'any'
	
	stages{
		stage('SCM Checkout'){
			steps{
			git branch: 'main', 
			url: 'https://github.com/duttdevops/sample-web-application-jenkins-docker.git'
			}
				}
		stage('Build Maven'){
			steps{
				def mvn= tool name: 'Maven3', type: 'maven',
				sh " ${mvn}/bin/mvn clean package "
		
			
			}
		}
	
	
	
	}



}
