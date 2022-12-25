pipeline{
    agent any
    stages{
        stage ("Stage1"){
            when {
                changelog ".*Update.*"
            }
            steps {
                echo "Hello from stage 1"
            }
        }
        stage ("Stage2"){
            steps {
                echo "Hello from stage 2"
            }
        }
    }
}