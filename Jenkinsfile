pipeline {
    agent any

    stages {
        stage('Checkout') {
		steps {	
		echo 'Checking out repo..'
		checkout scm
		sh("pwd")
		sh("ls")
		echo 'Checked out repo...'
		
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
		    	sh("ls -a")
			sh("pwd")
			sh("cd")
		    	sh("chmod +x ${WORKSPACE}/dev/devRelease.sh")
	 	    	sh("${WORKSPACE}/dev/devRelease.sh")
		    	echo 'Release to QA'
		    }
		    
		    
	    }
    }
}
	    
    
