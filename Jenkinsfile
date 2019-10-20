pipeline {
    agent any
    tools {
        maven '/opt/apache-maven-3.6.2' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn package'
            }
        }
        
        
    }
}
