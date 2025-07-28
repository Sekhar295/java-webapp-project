pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                echo 'SCM checkout'
                git 'https://github.com/Sekhar295/java-webapp-project.git'
            }
        }
        stage('build the code') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('deployment'){
            steps{
                sh 'sudo cp /var/lib/jenkins/workspace/scm pipeline/target/*.war /home/ubuntu/apache-tomcat-9.0.107/webapps'
            }
        }
    }
}
