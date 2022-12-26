pipeline{
    agent any
<<<<<<< HEAD
    stages{
        stage ("Stage1"){
=======
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("Stage1") {
            when {
                changelog ".*QA.*"
            }
            steps {
                echo "Hello from Stage 1 QA"
            }
        }
        stage("Stage2"){
            when {
                changelog ".*PROD.*"
                    
            }
            steps {
                 echo "Hello From Stage 2"
            }          
        }
        stage("Stage3"){
>>>>>>> 5853deaba3c6884eb074bccc73506ed070e7ebe0
            when {
                changelog ".*DEV.*"
            }
            steps {
<<<<<<< HEAD
                echo "Hello from stage 1"
            }
        }
        stage ("Stage2"){
            steps {
                echo "Hello from stage 2"
=======
               echo "Hello From Stage 3"
>>>>>>> 5853deaba3c6884eb074bccc73506ed070e7ebe0
            }
        }
    }
}