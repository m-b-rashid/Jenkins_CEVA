pipeline {
    agent any

    stages {
        stage('Checkout') {
		steps {	
		echo 'Checking out repo..'
		checkout scm
		}
	}
	    
	
       			       
        stage('Get-Users') {
		steps{
             	echo 'Getting Users..'
		script {
			 def roles = readFile("${WORKSPACE}/roles.csv")
			 echo(roles)
			}
		}
	}
	   
	  stage('Get-Images') {
		 steps{
		  echo 'Getting images..' 
			 script{
		  		sh 'curl -X GET http://localhost:8088/semarchy/api/rest/admin/image-libraries/ -u semadmin:semadmin'
		  		//sh("curl -s -k -X GET –header Content-Type: application/json’ \
        	  		  //–header ‘Accept:application/json’  \
		  		  //-header Authorization: Basic c2VtYWRtaW46c2VtYWRtaW4= \
		   		  //http://83.137.230.170/semarchy/api/rest/admin/image-libraries/")
			 }
		 	}	
	  }
    }
}
	    
    
