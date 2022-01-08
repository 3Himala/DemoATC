pipeline {
    agent any

    stages {
        stage('continous download') {
            steps {
                git 'https://github.com/3Himala/DemoATC.git'
            }
        }
        stage('continous build') {
            steps {
                sh 'mvn install'
            }
        }
       stage('continous deploy') {
            steps {
                sh 'scp target/DemoATR.war himala@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        } 
    }
}
