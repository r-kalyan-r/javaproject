pipeline{
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("QA-Stage") {
            when {
                changelog ".*QA.*"
            }
            steps {
                echo "executing QA script"
            }
        }
        stage("Prod-Stage"){
            when {
                changelog ".*PROD.*"
                    
            }
            steps {
                 echo "executing Prod script"
		 }          
        }
	stage("Prod-Dev"){
            when {
                changelog ".*Dev.*"

            }
            steps {
                 echo "executing Dev script"
                 }
        }
    }
}
