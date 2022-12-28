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
	//agent any
	//agent { docker { image 'maven:3.6.3'} }
	agent { docker { image 'node:3.6.3'} }
	stages {
		stage( 'Build' ) {
			steps {
				//sh 'mvn --version'
				sh 'node --version'
				echo "Build"
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