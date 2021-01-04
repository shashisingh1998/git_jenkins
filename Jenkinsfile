pipeline {
	    agent any
	    tools {
	        maven 'maven'
	        }
	    stages {
	        stage ('Compile') {
	            steps {
	                sh 'mvn compile'
	                }
	            }      
	        stage ('Package') {
	            steps {
	                sh 'mvn package'
	                }
	            }
	        stage ('Install') {
	            steps {
	                sh 'mvn install'
	                }
	            }
		stage ('Deploy check') {
                        steps {
                                sh "sudo -i"
                        }
                }
                stage ('Deploy War File') {
                        steps {
                                sh "cp helloworld.war /root/home/apache-tomcat-9.0.41/webapps/"
                        }
                }
	}
}
   
