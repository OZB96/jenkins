pipeline {
    agent { docker { image 'bryandollery/terraform-packer-aws-alpine' } }
    options {
        skipStagesAfterUnstable()
    }
    stages {
    stage('CreateDockerFile'){
	    steps {
		sh 'echo "FROM bryandollery/terraform-packer-aws-alpine" > "/Dockerfile"'
//		sh 'echo "RUN echo  \"<BuilderName>Omar Bazaid</BuilderName>\" > \"/Manifest.txt\"" >> /Dockerfile'
//		sh 'echo "RUN echo \"<BuildNumber>\${BUILD_NUMBER}</BuildNumber>\" >> \"/Manifest.txt\"">> /Dockerfile'
//		sh 'echo "RUN echo \"<DateTime>echo \$(date)</DateTime>\" >> \"/Manifest.txt\"" >> /Dockerfile'
		sh 'echo "RUN echo aa > /Manifest.txt" > "/Dockerfile"'    
	}
	}
   stage('BuildDockerfile') {
            steps {
		sh 'docker build --tag omar:\${BUILD_NUMBER /}'
                echo "Done ${cat /Manifest.txt}"
            }
        }
        }
}
