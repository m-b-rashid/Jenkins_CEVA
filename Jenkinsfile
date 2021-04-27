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
				 def images = readFile("${WORKSPACE}/about-dialog-logo.png")
				 //echo(images)
			 }
		 }	
	  }
	    stage('Build-Release') {
		 steps{
		 echo 'Build Release'
		  
			 }
		 	
	  }
	    stage('Test') {
		    steps{
		    echo 'Testing...'
		    }
	    }
	    stage('Dev-Release') {
		    steps {
	 	    sh ("dev/devRelease")
		    echo 'Relase to QA'
		    }
		    
		    
	    }
    }
}
	    
    
