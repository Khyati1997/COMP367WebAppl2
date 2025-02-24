pipeline {
    agent any

    environment {
        MVN_HOME = '/usr/share/maven'  // Adjust this if your Maven path is different
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Khyati1997/COMP367WebAppl2.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'mvn tomcat7:deploy'
            }
        }
    }
}
