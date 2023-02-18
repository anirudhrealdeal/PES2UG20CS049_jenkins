pipeline {
    agent any
    stages {
        stage( 'Build') {
            steps {
                sh 'g++ -o PES2UG20CS049 hello.cpp'
                ech 'Build Stage Successful '
            }
        }
        stage( 'Test') {
             steps {
                sh './PES2UG20CS049'
                echo 'Test Stage Successful '
             }
        }
        stage( 'Deploy') {
            steps {
                //this is intentional error
                echo 'Deployment Successful '
            }
        }
    }
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
