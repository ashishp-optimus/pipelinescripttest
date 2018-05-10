pipeline {
   agent none
    stages {
      
    stage('Test') { 
	agent { label 'cd-env' }
            steps {
                node {
   notifyStarted()
   /* ... existing build steps ... */
}

	   emailext (
      		   
      subject: "STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
      to: 'ashish.pandey@optimusinfo.com',
      body: """<p>STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
        <p>Check console output at "<a href="${env.BUILD_URL}">${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>"</p>""",
      recipientProviders: [[$class: 'DevelopersRecipientProvider'],]
    )
        }
	}
    }
} 
