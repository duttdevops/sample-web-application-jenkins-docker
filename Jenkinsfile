pipeline {
    agent none
    stages {
        stage('scm checkout') {
            steps {
		 git branch: 'main', 
		 url: 'https://github.com/duttdevops/sample-web-application-jenkins-docker.git'
                
            }
        }
	 stage('build code') {
            steps {
		 def mvnhome =tool name: 'Maven3', type: 'maven'
	         sh "${mvnhome}/bin/mvn clean package"  
                
            }
        }
    }
}
