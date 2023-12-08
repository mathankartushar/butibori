pipeline {
	agent any 
	triggers {
  pollSCM '* * * * *'
}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/tushar28/Downloads/apache-maven-3.9.5/bin/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/maxlife.war /home/tushar28/Downloads/apache-tomcat-9.0.82/webapps'
			}}	
}}
