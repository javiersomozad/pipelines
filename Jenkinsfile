#!groovy

pipeline {
	agent {
		node {
			label 'master'
		}
	}
    stages {
        stage('Primera fase') {
            steps {
                echo 'Ejecutando primera fase'
            }
        }
    }
    post {
        always {
            echo 'Al final siempre ejecuto esta pase lo que pase'
        }
    }
}
