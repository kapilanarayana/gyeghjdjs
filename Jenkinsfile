pipeline {
    agent any

    stages {
        stage('continous download ') {
            steps {
                git 'https://github.com/boxfuse/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('continous build ') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continous deployment ') {
            steps {
                sh 'sshpass -p "karthik" scp target/hello-1.0.war karthik@172.17.0.3:/opt/apache-tomcat-9.0.62/webapps'
            }
        }
    }
}

