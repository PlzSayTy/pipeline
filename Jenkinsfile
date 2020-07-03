pipeline {
    agent any

    stages {
	stage ('Run jar file stage') {

            steps {
                bat 'start.bat'
            }
        }
		stage('Checkout external proj'){
			
                  steps {

        git([
            url: "https://github.com/PlzSayTy/restAssuredExample.git",
            branch: 'master'
            //credentialsId: 'bd:c4:d5:78:c8:4d:db:92:89:68:dc:bf:d3:50:29:50'      
	])
  }
		}
	 
 
        stage ('Compile stage') {

        	steps {
                bat 'mvn clean compile'
            }
        }

        stage ('Testing stage') {

        	steps {
        		bat 'mvn clean test'
            }
        }
	stage ('Stop jar file stage') {

            steps {
                bat 'stop.bat'
            }
        }
	    stage('reports') {
    steps {
    script {
            allure([
                    includeProperties: false,
                    jdk: '',
                    properties: [],
                    reportBuildPolicy: 'ALWAYS',
                    results: [[path: 'target/allure-results']]
            ])
    }
    }
}

    }
}
