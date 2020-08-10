pipeline {
    agent { docker { image 'bryandollery/terraform-packer-aws-alpine' } }
    options {
        skipStagesAfterUnstable()
    }
    stages {
    stage('CreateDockerFile'){
	    steps {
		// sh "echo 'FROM bryandollery/terraform-packer-aws-alpine:latest' >> './Dockerfile'"
		writeFile file: '/Dockerfile', text: 'FROM bryandollery/terraform-packer-aws-alpine'
		// sh "echo 'RUN echo aa > /Manifest.txt >> ./Dockerfile'"   
		writeFile file: '/Dockerfile', text: 'RUN echo  "<BuilderName>Omar Bazaid</BuilderName>" >> /Manifest.txt'
	}

	}
   stage('BuildDockerfile') {
            steps {
		sh "docker build --tag omar:/${BUILD_NUMBER ./}"
                // echo "Done ${cat /Manifest.txt}"
            }
        }
        }
}
