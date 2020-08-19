pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
    stage('CreateDockerFile'){
	    steps {
		echo "building program shoukd be done here"
		}
	}

   stage('testing') {
            steps {
		echo "testing should be done here"
            }
        }
   stage('deploying') {
            steps {
		echo "deploying should be here"
            }
        }
 
        }
}
