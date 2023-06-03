#!groovy

pipeline {
	agent {
		node {
			label 'master'
		}
	}
    environment {
        CLAVE = 'valor'
    }
    stages {
        stage('Fase uno') {
            environment {
                CLAVE_FASE_UNO = 'Valor de fase uno'
            }
            steps {
                echo 'Primer step ejecutado. Mostrando variables'
                sh 'printenv'
            }
        }
    }
    post {
        always {
            echo 'Al final siempre ejecuto esta pase lo que pase'
        }
    }
}
