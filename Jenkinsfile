pipeline{
	agent any
	stages{
		stage('Build Application'){
			bat 'mvn clean install'
		}
		stage('Deploy Application to MuleSoft Cloudhub'){
			bat 'mvn package deploy -DmuleDeploy'
		}
	}
}