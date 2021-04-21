pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		 bat 'start https://github.com/icedwizz/Jenkins_CEVA/readme.txt'
				
				
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
