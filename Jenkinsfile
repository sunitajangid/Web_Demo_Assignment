pipeline {
    agent any
	
	stages {
		
		stage ('Stage 1 - Deploy the server') {
			steps {
				echo 'Starting the Demo Server'
				bat 'START "" python server.py'
			}
			stage ('Stage 2 - Start the test') {
			steps {
				echo 'Start the tests'
				bat 'robot --timestampoutputs --report report_webdemo --log log_webdemo --settag Application_Name:WebDemoOfTheMillenium --settag Version:1.0 login_tests'
			}
			
		}
	}
}
