pipeline {
    agent any
	parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }


    stages {
        stage('Clone Repository') {
            steps {
				echo 'clonie repo'
                //git 'https://github.com/nagireddy00/learn-jenk-nagi'
            }
        }

        stage('Build') {
            steps {
                // Commands to build your project, e.g., using Maven
                echo 'Building this pipeline'
            }
        }

        stage('Test') {
            steps {
                // Commands to run tests, e.g., using Maven
                echo 'testing this code'
            }
        }

        stage('Deploy') {
            steps {
                // Commands to deploy your application, e.g., copying files to a server
                echo 'deploy this code'
            }
        }
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
		always {
			echo 'Pipeline runs always'
		}
    }
}
