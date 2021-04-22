pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		    script {
			def inputCSVPath = input message: 'Upload file', parameters: [file(name: 'dev/roles.csv', description: 'Upload only CSV file')]
			def csvContent = readFile "${inputCSVPath}"
                        echo ("CSV FILE PATH IS : ${inputCSVPath}")
			echo("CSV CONTENT IS: ${csvContent}")
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
