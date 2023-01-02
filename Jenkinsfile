pipeline {
	  agent any
	  
	  environment {
	       dockerHome = tool "myDocker"
		   mavenHome = tool "myMaven"
		   PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	  }
	  stages {
	     stage('Build') {
		      steps {
			  
			    sh 'maven --version'
				sh 'docker --version'
				echo 'Build'
				echo "PATH - $PATH"
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "JOB_NAME - $env.JOB_NAME"
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
