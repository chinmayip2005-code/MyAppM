pipeline{
	agent any
	}
tools{
	maven 'Maven'
	}
Stages{
	stage('Checkout'){
		steps{
		git branch:'main', url: 'https://github.com/chinmayip2005-code/MyAppM.git'
		}
		}
	stage('Build'){
		steps{
		sh 'mvn clean package'
		}
		}
	stage('Test'){
		steps{
		sh 'mvn test'
		}
		}
	stage('Run Application'){
		steps{
		sh 'java -jar target/MyMApp-1.0-SNAPSHOT.jar'
		}
		}
	}
	post{
		success{
		echo 'Build succcessful'
		}
		failure{
		echo 'Build failure'
		}
		}
		}
			
