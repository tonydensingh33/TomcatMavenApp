pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven-3.9.8"
    }
    stages {
        stage('scm') {
            steps {
                // Get the code from a GitHub repository
                git 'https://github.com/tonydensingh33/TomcatMavenApp.git'
            }
        }
        stage('Build') {
            steps {
                //Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
