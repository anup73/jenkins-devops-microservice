pipeline {
	  agent { docker { image 'maven:3.8.6'} }
	  stages {
	     stage('Build') {
		      steps {
			    sh 'mvn --version'
				echo 'Build'
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
