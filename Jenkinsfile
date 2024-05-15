pipeline{
	agent {
		label 'blue'
		}
	environment{
	JAVA_HOME = '/home/grras/project/jdk-11.0.21'
		}	

	stages{
		stage("Checkout"){
			steps{
			checkout scm
				}
			}
		stage("Build"){
			steps{
			  sh '/home/grras/project/apache-maven-3.9.6/bin/mvn install'					}
				}
		stage("Deployment"){
			steps{
			sh 'cp target/Mustard.war /home/grras/project/apache-tomcat-9.0.89/webapps'
				}
				   }	
		}
	}
