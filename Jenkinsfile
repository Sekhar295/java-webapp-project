pipeline {
    agent { label 'slave1' }

    stages {
        stage('SCM_Checkout') {
            steps {
                echo 'Perform SCM_Checkout'
				git 'https://github.com/Sekhar295/java-webapp-project.git'
            }
        }
        stage('Application_Build') {
            steps {
                echo 'Perform Application_Build'
				sh 'mvn clean package'
            }
        }
        stage('Deploy to Target Server') {
            steps {
                echo 'Perform Deployment'
            }
        }
    }
}
