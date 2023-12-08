pipeline {
	agent any 
	parameters {
  choice choices: ['haircut', 'beard', 'massage'], name: 'saloon'
}

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
			  sh '/home/tushar28/Downloads/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/butibori.war /home/tushar28/Downloads/apache-tomcat-9.0.82/webapps'
			}}	
}}
