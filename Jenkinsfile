pipeline{
	agent{
		docker{image: 'fabrica:1.0'}
	}
	stages{
		stage('Test'){
			steps{
				sh 'fabrica --version'
			}
		}
	}
}	
