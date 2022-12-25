pipeline {
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("Stage1") {
            when {
                 changelog '.*^\\[added\\] .+$' 
            }
            steps {
                echo "Hello from Stage one"
            }
        }
        stage("Stage2"){
             when {
                changelog "downgrade"
            }
            steps {
                 echo "Hello From Stage 2"
            }          
        }
        stage("Stage3"){
              when {
                changelog ".*QA.*"
            }
            steps {
               echo "Hello From Stage three"
            }
        }
    }
}
