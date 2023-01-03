pipeline {
	  agent { docker { image 'maven:3.6.3'} }
	  
	  stages {
	     stage('Build') {
		      steps {
				echo 'Build'
				sh 'maven --version
				echo "PATH - $PATH"
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		 }
		 stage('Test') {
		      steps {
				echo 'Test'
			  }
		 }
		 stage('Integration Test') {
		      steps{
					echo 'Integration Test'
			}
		 }
	  } 
	  post {
		always {
			echo 'I run always'
		}
	  }
}
