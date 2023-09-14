pipeline {
    //agent any
    agent { node { label 'workstation' } }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                //error 'This is an error'
            }
        }

    }
    post {
        always{
            echo 'post'
            //send email
            //trigger some other job
            //update some jira status about the build
        }
    }
}
