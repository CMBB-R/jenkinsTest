pipeline {
    agent any

    stages {
        stage('run frontend') {
            steps {
                echo 'Exec yarn..'
		nodejs('Node-20-8-0') {
			sh 'yarn install' 
			}
		}
        }
        stage('run backend') {
            steps {
                echo 'Exec gradle..'
		withGradle() {
			sh './gradlew -v'
		}
            }
        }
        stage('Test') {
            steps {
                echo 'lala tested something....'
            }
        }
    }
}
