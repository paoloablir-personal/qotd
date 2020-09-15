pipeline {
	agent any
	stages {
		stage('Build Application') {
			steps {
				sh 'export MAVEN_HOME=/usr/local/Cellar/maven/3.6.1'
				sh 'export PATH=$PATH:$MAVEN_HOME/bin'
				sh 'mvn clean install'
			}
		}
		stage('Deploy Application to MuleSoft CloudHub') {
			steps {
				sh 'export MAVEN_HOME=/usr/local/Cellar/maven/3.6.1'
				sh 'export PATH=$PATH:$MAVEN_HOME/bin'
				sh 'mvn package deploy -DmuleDeploy'
			}
		}
	}
}