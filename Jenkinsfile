pipeline {
    agent any
    stages {
        stage("Test") {
            when {
                changelog ".*down*"
            }
            steps {
                echo "Hello World!"
            }
        }
    }
}
