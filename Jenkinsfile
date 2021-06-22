pipeline {
    agent any
    tools {
        maven "3.6.3"
    }
    stages {
        stage('Git CheckOut') {
            steps {
                git branch: 'main', credentialsId: 'My private token login creds', url: 'https://github.com/logicopslab/WebAppForJenkins.git'
            }
        }
        stage('Clean and Install') {
            steps {
               bat 'mvn clean install'
            }
        }
       
    }
}
