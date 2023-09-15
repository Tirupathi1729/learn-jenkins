pipeline {
    //agent any
    agent { node { label 'workstation' } }
    environment{
        Test_URl = "google.com"
        SSH = credentials("centos-ssh")
    }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                //error 'This is an error'
                echo Test_URl
                echo SSH
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
