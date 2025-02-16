pipeline {
	agent any
	parameters {
		string(name: 'ENV', defaultValue: 'staging', description: 'Target environment') 
		choice(name: 'DEPLOY_REGION', choices: ['us-east-1', 'us-west-2'], description: 'AWS Region') 
		booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Do you want Run tests before deployment?')
	}
	stages {
		stage('Build Script') {
			steps {
				script {
					echo "This is we are triggering Build Stage"
				}
			}		
		}
		stage('Test Script') {
			steps {
				script {
					if (params.RUN_TESTS == true) {
						echo "We are runnig testcase"
					}
				}
			}			
		}
		stage('Deploy') {
			steps {
				script {
					if (params.DEPLOY_REGION == "us-west-2") {
						echo "Deploying US West 2 Region"
					}
				}
			}
		}
	}
}
