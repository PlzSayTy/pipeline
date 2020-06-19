pipeline {
    agent any

    stages {

		stage('Checkout external proj'){
                  steps{
     
 git branch 'master',
     
 credentialsID: 'ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEAxsaRZw5Zd7oPLZx/C9ktvKrwXvbYl6Zoprm3DafnYpn9ZDs9nQ4oWkRg22RTmnx28ItpDSwiHwENiKzPPW6U/vpapNJRYyVFVizSq+AIidRySldjuoqyViDo2uDt6gDTIQxHXoPyVTrKRAckdcf0wsr7rJzOThwMK195SHTTPfrGoM+qZX2eQnYq/XRDyEQNxoW6j5eorg/RQHUcDBLQEdaG8eagd9Xq+iBgGonPM5KePxldu4VOWAYvwXVYSBqZnsd0+p4wuLUsHOpnpmFIFtUTarxuGePrwZKmsC4VQye+jLsTVCI0hgq1ojTeuyfJ98zX5Ope/0q/wWGcazyR1w== rsa-key-20200618',
  
    url: 'git@github.com:PlzSayTy/CalculatorAplication.git',
    
  sh 'ls -lat'
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
