pipeline {
    agent any
    stages {
        stage("Stage1") {
            when {
            changelog ".*Update.*"
            }
            steps {
                echo "Hello from Stage1"
            }
        }
        stage("Stage2"){
            steps {
                 echo "Hello From Stage2"
            }          
        }
        stage("Stage3"){
            steps {
               echo "Hello From Stage3"
            }
        }
    }
}
