environment{
    Test_URl = "google.com"
    }
pipeline {
    //agent any
    agent { node { label 'workstation' } }
//     environment{
//     Test_URl = "google.com"
//     }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                //error 'This is an error'
                echo Test_URl
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
