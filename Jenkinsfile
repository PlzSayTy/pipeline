pipeline {
    agent any

    stages {

		stage('Checkout external proj'){
			
                  steps {

        git([
            url: "git@github.com:PlzSayTy/CalculatorAplication.git"
            //branch: 'master',
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
        		bat 'mvn test'
            }
        }

    }
}
