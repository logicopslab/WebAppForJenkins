pipeline {
    agent any

    stages {
        stage('Copy repo') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/Novman47/WebAppForJenkins.git'
            }
        }
        stage('Build Artifact') {
            steps {
                // Run Maven on a Unix agent.
                sh "mvn clean install"
            }
        }
        stage('Build Package') {
            steps {
                // Run Maven on a Unix agent.
                sh "mvn package"
            }
        }
    } // <-- add this closing curly brace to close the 'stages' block
}
