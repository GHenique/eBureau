pipeline {
    agent any 
    
    tools {
        maven 'M3'
    }
    
    stages {
        stage('Compile') { 
            steps {
                // 
                echo 'Etape Compile'
                bat 'mvn clean compile'
            }
        }
        stage('Test') { 
            steps {
                //
                echo 'Etape Test'
                bat 'mvn clean test'
            }
        }
        stage('Packaging') { 
            steps {
                // 
                echo 'Etape Packaging'
                bat 'mvn clean package'
            }
        }
        stage('Deploy') { 
            steps {
                // 
                echo 'Etape Deploy'
                bat 'copy /Y "target\\ebureau.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 9.0\\webapps"'

            }
        }
        
    }
}
