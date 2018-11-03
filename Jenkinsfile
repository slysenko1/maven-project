pipeline {
    agent any
    stages{
        stage ('Initialize') {
            steps {
                sh  'export PATH=/var/jenkins_home/apache-maven-3.6.0/bin:$PATH'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
}