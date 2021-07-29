pipeline {
    agent none
	tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven3"
    }
    stages {
        stage('scm checkout') {
            steps {
		 git branch: 'main', 
		 url: 'https://github.com/duttdevops/sample-web-application-jenkins-docker.git'
                
            }
        }
	 stage('build code') {
            steps {
	        sh " mvn clean package "  
                
            }
        }
    }
}
