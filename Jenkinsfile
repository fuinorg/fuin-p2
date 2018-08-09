pipeline {
    agent any 
    tools { 
        jdk 'Oracle JDK 8 (latest)'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh "./mvnw -version"
            }
        }
        stage('Build') { 
            steps {
                sh "./mvnw clean deploy -U -B -s /private/jenkins/settings.xml" 
            }
        }
    }
}
