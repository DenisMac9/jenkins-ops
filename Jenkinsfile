pipeline {

    agent {
	  label "autoscale"
    }

    triggers {
        pollSCM('*/1 * * * *')
    }
    
    options { disableConcurrentBuilds() }
    
    stages {

        stage ('Checkout') {
            steps {
                checkout scm
            }
        }

        stage ('Deployment') {
            steps {
		docker.withServer('tcp://10.135.107.29:2376') 
        	sh 'docker stack deploy -c docker-compose.yml votingapp'
		
		}
        }

    }
}

