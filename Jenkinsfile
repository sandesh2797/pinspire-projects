pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                // Compile the Java code using javac
                sh 'javac hello.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                sh 'java hello'
            }
        }
    }

    post {
        success {
            echo 'Java code is compiled and run successfully!'
        }
        failure {
            echo 'Compilation or execution of Java code failed. Please check the logs for details.'
        }
    }
}
