pipeline {
    agent { docker { image 'bryandollery/terraform-packer-aws-alpine' } }
    options {
        skipStagesAfterUnstable()
    }
    stages {
    stage('CreateDockerFile'){
	    steps {
		echo "creating Dockerfile"
		sh "echo 'FROM bryandollery/terraform-packer-aws-alpine:latest' >> '/Dockerfile'"
		sh "echo 'RUN echo aa > /Manifest.txt >> /Dockerfile'"   
	}
	}
   stage('BuildDockerfile') {
            steps {
		sh 'docker build --tag omar:\${BUILD_NUMBER /}'
                //echo "Done ${cat /Manifest.txt}"
            }
        }
        }
}
