pipeline {
   agent none
    stages {
      
    stage('Test') { 
	agent { label 'cd-env' }
            steps {
                // Steps to execute scripts
		
	   emailext (
      mail (to: 'ashish.pandey@optimusinfo.com',		   
      subject: "STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
      body: """<p>STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
        <p>Check console output at "<a href="${env.BUILD_URL}">${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>"</p>""",
      recipientProviders: [[$class: 'DevelopersRecipientProvider'],]
    )
        }
	}
    }
} 
