	pipeline {
	agent none
	stages {
		stage('Build') {
          agent {label 'node1'}
					steps {
						sh 'sleep 15; echo "This is a Build stage"'
					}
				}
				
				stage('Test'){
          agent {label 'node2'}
					steps {
						sh '''
							sleep 15
							echo "This is a Test stage"
						'''	
						git branch: 'main', url: 'https://github.com/RPJdevops/pipeline-job.git'
					}
				}
		stage('Deploy'){
      agent {label 'node1'}
			steps {
				sh '''
					sleep 5
					echo "This is a Deploy stage"
				'''
			}
		}
	}
	}
