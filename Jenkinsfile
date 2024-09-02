pipeline {
	agent{
	label 'newlabel'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh 'JAVA_HOME=/home/newgrras/newdir/jdk-11.0.24 /home/newgrras/newdir/apache-maven-3.9.8/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/multibranchrepo.war /home/newgrras/newdir/apache-tomcat-9.0.93/webapps'
			}}	
}}
