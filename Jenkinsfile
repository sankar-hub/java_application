pipeline {
    agent any
    tools {
        maven 'M2_HOME' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'sudo -su root'
                sh 'mvn package'
            }
        }
       stage('SonarQube analysis') { 
             steps {
                sh 'mvn clean install'
                withSonarQubeEnv('sonar') { 
                sh 'mvn sonar:sonar'
                }
        }
        } 
        
    }
}
