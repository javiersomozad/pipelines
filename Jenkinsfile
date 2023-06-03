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
                CREDENCIALES_FASE_UNO = credentials('misCredenciales')
            }
            steps {
                echo 'Primer step ejecutado. Mostrando variables'
                // sh 'printenv'
                sh 'echo "Usuario : $CREDENCIALES_FASE_UNO_USR"'
                sh 'echo "Pass : $CREDENCIALES_FASE_UNO_PSW"'
                sh 'echo "Credenciales $CREDENCIALES_FASE_UNO"'
            }
        }
    }
    post {
        always {
            echo 'Al final siempre ejecuto esta pase lo que pase'
        }
    }
}
