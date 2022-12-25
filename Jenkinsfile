pipeline {
    agent any
    stages {
        stage("Checkout"){
        steps {
            checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: 'https://github.com/r-kalyan-r/javaproject.git',credentialsId: 'git-token']], branches: [[name: 'main']]], poll: false
          }
        }
        stage("Stage1") {
            steps {
                echo "Hello from Stage 1"
            }
        }
        stage("Stage2"){
            steps {
                 echo "Hello From Stage 2"
            }          
        }
        stage("Stage3"){
            steps {
               echo "Hello From Stage 3"
            }
        }
    }
}
