pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
              git 'https://github.com/efsavage/hello-world-war.git'
            }
        }
         stage('cb') {
            steps {
               sh 'mvn install'
            }
        }
         stage('cdp') {
             steps
             {
        sh 'sshpass -p "kiran" scp target/hello-world-war-1.0.0.war kiran@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
 }

