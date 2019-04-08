pipeline{
	agent any
	stages{
		stage("Grid Init"){
			steps{
				sh "docker-compose up --no-color -d hub chrome firefox"
				}
			}
		stage('Test Execution'){
			steps{
				sh "docker-compose up search-module book-flight"		
				}
			}
	}
		post{
			always{
				archiveArtifacts artifacts: 'output/**'
				sh "docker-compose down"
				}
			}
	}

