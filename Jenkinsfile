pipeline {
    agent any

    stages {

		stage('Checkout external proj'){
			
                  steps {

        git([
            url: "git@github.com:PlzSayTy/CalculatorAplication.git",
            branch: 'master',
            credentialsId: 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDDj1vhP3M3KXT4whOA/NpqHGsrXr/bKrfQjA5dzgixSCKDz2Omg7Q5mlchPEKstjLoASxUMRmWC5NeFgmCdrpiA13YNrGp+oWTmYf22ZEWx10z7eorxm1/gu2rDQEwsesPb8KJ8xa2DvXp2/VnE0vZZ9rYvnkt0Kf+Tk0sCEtQiHSxIJnpQ2VKmRtVLkEsXcSQn5hGf2n4UazfC43G7+z1/0qBATCHqHVsqh5wxV91lCiApaVgXtDAV5ONEkdrjeuo1r9LpZvHrN1q5z/bRhKcHaHtGONKGd5rKxLpm4I0qcZLFDX7bk3Zqc9FPDG0EP7b3HtdFWJwG5LBWDHPWrppOytDd+Q3yS4z4xPXNqbYFZ/21rPenJnMQwvoStyyF2JGA7+SUbtyx5Jey/E51TKAE2VPDqtrQURKPeXP8DzkGtW/LxmSoXXKdHENLm19nPniZ68JexhGNfzUBNQhYVqiH7wl2of3BXT8h2ohpHKZy7Jn62yj0CEo/YsaEvxcb4B+nBilqJWhiVQ1/bdJaIIgdzre3sOLnXKdUNQsX63+kvpZRK4JpWi8LzT8B/rcV48f+flfgGBcDQ/i/rYRr5hw5l7dCQMKjaJerTleMoybMWHlE4KZ7HyRZiOC6UYjkfy3HJsXv2ViqBG40GS1PYIj96QQBzgIn8dq/oju1RIrWw== trubetskoyvladimir@yandex.ru'
'
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
