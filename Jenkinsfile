pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    script {
			checkout scm
			sh("ls") 
			
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
