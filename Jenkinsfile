
pipeline
	{
	agent { label 'master' }
	// The options directive is for configuration that applies to the whole job.
	environment {
		// update the project name variable with  Project repository name
		ProjectName = 'test'
	}
	options {
			// For example, we'd like to make sure we only keep 10 builds at a time, so
			// we don't fill up our storage!
		buildDiscarder(logRotator(numToKeepStr:'5'))

			// And we'd really like to be sure that this build doesn't hang forever, so
			// let's time it out after an hour.
		timeout(time: 60, unit: 'MINUTES')
		}
    //parameters {
	//	 choice(
      //      choices: 'Yes\nNo',
        //    description: 'Upload the build artifacts for VeracodeScan',
          //  name: 'Veracode_Scan')
    }
	stages {
		stage('Build') {
            steps {
				echo 'Pulling...' + env.BRANCH_NAME
				sh 'build.sh'		
				}

			
			}
		}
	}
