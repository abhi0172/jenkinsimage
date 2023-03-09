pipeline {
	agent {	
		label 'docker_agent'
		}
	stages {
		stage("SCM") {
			steps {
				git 'https://github.com/abhi0172/jenkinsimage.git'
				}
			}
  	stage("Image") {
			steps {
				sh 'sudo docker build -t jenkinsbuild .'
				sh 'sudo docker tag java-repo:$BUILD_TAG abhishek0322/jenkinsbuild:$BUILD_TAG'
				}
			}
