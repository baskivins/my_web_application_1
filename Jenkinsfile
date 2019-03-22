pipeline{

agent {label 'master'}

tools{
	maven 'maven'
	jdk 'jdk8'
}

stages{
	stage('build the project'){
		steps{
			bat 'mvn clean install'
		}
	}
	
	stage('send email'){
		steps{
			emailext attachLog: true, body: 'build success message or failure', subject: 'jenkins test build', to: 'baskaran.g@gmail.com'
		}
}
}
