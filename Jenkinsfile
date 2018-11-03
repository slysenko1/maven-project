pipeline {
    agent any
    tools {
        maven 'maven 3.6.0'

    }
    stages{
        stage ('Initialize') {
            steps {
                sh  'export PATH=/var/jenkins_home/apache-maven-3.6.0/bin:$PATH'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}