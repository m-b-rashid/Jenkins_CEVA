pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    checkout scm
		    script {
			
			bat "dir C:\\cygwin64\\bin\\bash.exe"
			sh 'ls..' 
		    }
		    
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
