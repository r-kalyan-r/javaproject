pipeline {
    agent any
    stages {
        stage("Stage1") {
            when {
                changelog ".*added.*"
            }
            steps {
                echo "Hello from Stage one"
            }
        }
        stage("Stage2"){
             when {
                changelog ".*downgrade.*"
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
               echo "Hello From Stage3"
            }
        }
    }
}
