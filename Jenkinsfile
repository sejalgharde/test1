pipeline {
	agent any 
	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/sejal/Documents/devops-software/apache-maven-3.9.5
/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/PROJECT1.war /home/sejal/Documents/devops-software/apache-tomcat-9.0.82/webapps
'
			}}	
}}
