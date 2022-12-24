pipeline {
    agent any
    stages {
        stage("Test") {
            when {
                changelog ".*Downgrade.*"
            }
            steps {
                echo "Hello World!"
            }
        }
    }
}
