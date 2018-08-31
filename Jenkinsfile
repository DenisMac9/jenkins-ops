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
                sh 'docker stack deploy -c docker-compose.yml votingapp'
            }
        }

    }
}

