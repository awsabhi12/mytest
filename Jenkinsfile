pipeline{
	agent any
	tools{
		maven 'Maven'
		}
	stages{
		stage('Checkout'){
		steps{
			git branch : 'master',url : 'https://github.com/awsabhi12/mytest.git'
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
		stage('Run Applicatiom'){
		steps{
			sh 'java -jar target/mytest-1.0-SNAPSHOT.jar'
			}
			}
			}
	post{
	success{
		echo 'building successful'
	}
	failure{
		echo 'build failed'
		}
		}
	}
