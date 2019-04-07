pipeline{
	agent any
	stages{
		stage("Grid Init"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
				}
			}
		stage('Test Execution'){
			steps{
				sh "docker-compose up search-module.xml book-flight-module.xml"		
				}
			}
	post(){

		}
	}
}
