pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
            git 'https://github.com/AneesRavidKhan/DemoATC.git'
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
       sh 'sshpass -p "kiran" scp target/DemoATR.war kiran@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
 }

