pipeline {
    agent {'any'} 
    stages {
        stage('scm checkout') {
            steps {
		    git branch: 'main', 
			url: 'https://github.com/duttdevops/sample-web-application-jenkins-docker.git'
                
            }
        }
	 stage('build code') {
            steps {
		 def mvn= tool name: 'Maven3', type: 'maven'
	         sh " ${mvn}/bin/mvn clean package "  
                
            }
        }
    }
}
