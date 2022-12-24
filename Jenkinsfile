pipeline {
    agent any
    stages {
        stage("Test") {
            when {
                changelog '.*^\\[Update\\] .+$'
            }
            steps {
                echo "Hello World!"
            }
        }
    }
}
