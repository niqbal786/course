pipeline{
	agent any
		stages {
			stage('Preperation'){
				steps{ sh 'docker pull ubuntu'
				       sh 'docker pull nginx'
				       sh 'docker pull tutum/hello-world'
					}
				}
			stage('build'){
				steps{ sh 'docker run -itd -p 82:80 --name kohli tutum/hello-world'
					}
				}
			stage('test'){
				steps{ echo 'this is testing stage'
					}
				}
			stage('deploy'){
				steps{ input ('Do you want to proceed?')
					echo 'this is deploy stage'
					}
				}
	}
}
