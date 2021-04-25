pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    checkout scm
		    	bat "dir C:\\cygwin64\\bin\\bash.exe"
			curl -s -k -X GET –header Content-Type: application/json’ \
        		–header ‘Accept:application/json’  \
		    	-header Authorization: Basic c2VtYWRtaW46c2VtYWRtaW4= \
		    	http://localhost:8088/semarchy/api/rest/admin/image-libraries/
		    
		    
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
