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
			 def roles = readFile("${WORKSPACE}/roles.csv").each { line ->
   			 line.each { field ->
			 echo(roles)
			}
		}
	}
    }
}
	    
    
