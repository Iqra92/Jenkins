pipeline {
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/Iqra92/Jenkins.git"
            }
        }
        stage("Build"){
            steps {
                dir("Jenkins") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                dir("Jenkins") {
                    sh "mvn test"
                }
            }
        }
    }
}