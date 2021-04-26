pipeline {
    agent any

    stages {
        stage('Checkout') {
		steps {	
		echo 'Checking out repo..'
		checkout scm
		}
	}
	    
	
       			       
        stage('Get-Roles') {
		steps{
             	echo 'Getting Roles..'
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
				 def images = readFile("${WORKSPACE}/images.png")
				 echo(images)
			 }
		 }	
	  }
	    stage('Test') {
		    
		    
	    }
	    stage('Release') {
		    
		    
	    }
    }
}
	    
    
