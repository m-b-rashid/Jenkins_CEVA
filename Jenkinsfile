pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    script {
		readCSV("dev/roles.csv")
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
