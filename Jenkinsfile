pipeline {
	agent any

	tools {
		maven "jenkin-maven"
  	     }


	stages {
		stage('scm') {
			steps {
				git 'https://github.com/ashwin1-dev/war-file-12dec23.git'
			      }
                           }

	        stage('build') {
			steps {

				sh 'mvn clean package'
                              }
                           }

               stage('deploy') {
		       steps {
				sh 'scp target/mob6-1.0.jar   192.168.10.32:/opt/apache-tomcat-9.0.91/webapps'
                             }
                           }
                 }
   }
