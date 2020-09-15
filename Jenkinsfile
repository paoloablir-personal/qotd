pipeline {
	agent any
	tools {
		maven 'Maven 3.6.1'
	}
	stages {
		stage('Build Application') {
			steps {
				sh 'mvn clean install'
			}
		}
		stage('Deploy Application to MuleSoft CloudHub') {
			steps {
				sh 'mvn package deploy -DmuleDeploy'
			}
		}
	}
}