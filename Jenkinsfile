// Scripted format
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage(' Integration Test') {
// 		echo "Integration Test"
// 	}
// }

// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Integration Test"
// }

//DECLARATIVE

pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'} }
	//agent { docker { image 'node:13.6'} }
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage( 'Build' ) {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
				echo "JOB_NAME - $env.JOB_NAME"
			}
		}
		stage( 'Test' ) {
			steps {
 				echo "Test"
			}	
		}
		stage( 'Integration Test' ) {
			steps {
 				echo "Integration Test"
			}
		}
	}
}