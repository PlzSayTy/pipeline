pipeline {
    agent any

    stages {

		stage('Checkout external proj'){
			
                  steps {

        git([
            url: "git@github.com:PlzSayTy/CalculatorAplication.git",
            branch: 'master',
            credentialsId: 'b8:80:1e:90:3d:79:45:d5:fc:50:b4:8d:e5:75:ab:a1'
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
