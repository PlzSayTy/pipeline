pipeline {
    agent any

    stages {
	
		stage('Checkout external proj'){
			
                  steps {

        git([
            url: "https://github.com/PlzSayTy/restAssuredExample.git",
            branch: 'master'
            //credentialsId: 'bd:c4:d5:78:c8:4d:db:92:89:68:dc:bf:d3:50:29:50'      
	])
  }
		}
	    node {
   bat 'C:\\Program Files (x86)\\Jenkins\\workspace\\Calculator_master_2\\web-db-0.0.1-SNAPSHOT.jar'
}
	    stage ('Start server') {

        	steps {
		
              
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
