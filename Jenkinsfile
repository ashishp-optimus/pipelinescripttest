pipeline {
   agent none
    stages {
      
    stage('Test') { 
	agent { label 'cd-env' }
            steps {
                // Steps to execute scripts
		
	     mail (to: 'ashish.pandey@optimusinfo.com',
         subject: "Job '${env.JOB_NAME}' (${env.BUILD_NUMBER}) is waiting for input",
         body: "Please go to ${env.BUILD_URL}.");
        }
	}
    }
} 
