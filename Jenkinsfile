pipeline {
    agent any

    stages {
        stage('Checkout') {
		echo 'Checking out repo..'
		checkout scm
	}
	    
	    stage('Get-Images') {
		  echo 'Getting images..'  
		    script {
		  		bat "dir C:\\cygwin64\\bin\\bash.exe"
		  		curl -s -k -X GET –header Content-Type: application/json’ \
        	  		–header ‘Accept:application/json’  \
		  		-header Authorization: Basic c2VtYWRtaW46c2VtYWRtaW4= \
		   		http://localhost:8088/semarchy/api/rest/admin/image-libraries/
					}	
		    
        }
        stage('Get-Users') {
            steps {
                echo 'Getting Users..'
		    script {
			    readFile("${WORKSPACE}/roles.csv")
		
            }
        }
      
        }
    }
}
