#!groovy

pipeline {
	agent {
		node {
			label 'master'
		}
	}
    parameters {
        string(name: 'NOMBRE', defaultValue: 'Mario', description: 'Cual es tu nombre?')
        text(name: 'APELLIDO', defaultValue: 'Moreno', description: 'Y tu apellido?')
        booleanParam(name: 'BOOLEANO', defaultValue: true, description: 'Ejemplo booleano')
        choice(name: 'ELECCION', choices: ['Primero', 'Segundo', 'Tercero'], description: 'Elige')
        password(name: 'PASSWORD', defaultValue: 'secreto', description: 'Indica la contraseña')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.NOMBRE}"
                echo "Apellido: ${params.APELLIDO}"
                echo "Toggle: ${params.BOOLEANO}"
                echo "Choice: ${params.ELECCION}"
                echo "Password: ${params.PASSWORD}"
            }
        }
    }
    post {
        always {
            echo 'Al final siempre ejecuto esta pase lo que pase'
        }
    }
}
